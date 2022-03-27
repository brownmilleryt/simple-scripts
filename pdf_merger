# -*- coding: utf-8 -*-
"""
@author: dsierant
"""

"""
Argumenty przekazywane do skryptu. Ścieżka 1 pliku.pdf, ścieżka 2 pliku .pdf, ścieżka do zapisu, nazwa sprawozdania
Część programu do zapisywania i raportowania wyników badań
"""
import sys
import shutil
from pdfrw import PdfReader, PdfWriter
writer = PdfWriter()

formatP = ".pdf"
sciezkapdf1 = r"\\xxx\Users\dsierant\Desktop\xxx\xxx\Kopie_Wyników\\"
sciezkapdf2 = r"\\xxx\protok\ZBiMW\\"
sciezkazapisu = r"\\xxx\Users\dsierant\Desktop\xxx\xxx\AUTORYZACJA\\"


pdf1 = sciezkapdf1 + sys.argv[1]                                #Wynik
pdf2 = sciezkapdf2 + sys.argv[2] + "_p.pdf"                     #Protokół
pdf3 = sciezkapdf2 + sys.argv[2] +  "_z.pdf"                     #Zlecenie
sciezkapdf = sciezkazapisu + sys.argv[3]
nazwapdf = "Połączone(Prot+zlec)_Sprawozdanie nr " + sys.argv[4]


files = [pdf3,pdf1,pdf2]

link = sciezkapdf

for fname in files:
    writer.addpages(PdfReader(fname).pages)
    writer.write(link + nazwapdf + formatP )

dst = link + "/Sprawozdanie nr " + sys.argv[4] + ".pdf"

shutil.copy2(pdf1,dst)