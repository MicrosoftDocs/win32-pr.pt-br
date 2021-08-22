---
description: Este tópico lista os construtores da classe Metafile. Para uma listagem de classe completa, consulte Classe metafile.
ms.assetid: a9648287-65d9-47d8-b32b-33f74b4fcd07
title: Construtores Metafile.Metafile
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9a993cb8d0e21e57fe495e5948546ab8ea51e2829af3bd42b962a0be9408e419
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977846"
---
# <a name="metafilemetafile-constructors"></a>Construtores Metafile.Metafile

Este tópico lista os construtores da classe [**Metafile.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile) Para uma listagem de classe completa, consulte **Classe Metafile**.

### <a name="overload-list"></a>Lista de sobrecargas



| Construtor                                                                                                                                                                      | Descrição                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Metafile(WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar))                                                                                                          | Cria um [**objeto Metafile::Metafile**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar)) para reprodução.<br/>                                                                                                                                                   |
| [**Metafile(IStream \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream))                                                                                                          | Cria um [**objeto Metafile::Metafile**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream)) de uma interface [IStream](/windows/win32/api/objidl/nn-objidl-istream) para reprodução.<br/>                                                            |
| [**Metafile(HEN BOOAFILE,BOOL)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhenhmetafile_inbool))                                                                                          | Cria um GDI+ [**metafile::metafile**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhenhmetafile_inbool)) para reprodução com base em um arquivo EMF (Metadado Avançado) GDI.<br/>                                                                                            |
| [**Metafile(HDC,EmfType,WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inemftype_inconstwchar))                                                                         | Cria um [**objeto Metafile::Metafile**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inemftype_inconstwchar)) para gravação.<br/>                                                                                                                             |
| [**Metafile(WCHAR, \* HDC, EmfType,WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inemftype_inconstwchar))                                                        | Cria um [**objeto Metafile::Metafile**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inemftype_inconstwchar)) para gravação.<br/>                                                                                                                    |
| [**Metafile(IStream, \* HDC, EmfType,WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inemftype_inconstwchar))                                                        | Cria um [**objeto Metafile::Metafile**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inemftype_inconstwchar)) para gravação em uma interface [IStream.](/windows/win32/api/objidl/nn-objidl-istream)<br/>                               |
| [**Metafile(HMETAFILE,WmfPlaceableFileHeader,BOOL) \***](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhmetafile_inconstwmfplaceablefileheader_inbool))                                             | Cria um GDI+[**metafile::metafile**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhmetafile_inconstwmfplaceablefileheader_inbool)) para gravação. O formato será um metarquivo acessível.<br/>                                                                          |
| [**Metafile(HDC,Rect&,MetafileFrameUnit,EmfType,WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar))            | Cria um [**objeto Metafile::Metafile**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar)) para gravação.<br/>                                                                                        |
| [**Metafile(HDC,RectF&, MetaFileFrameUnit, EmfType,WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar))           | Cria um [**objeto Metafile::Metafile**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar)) para gravação.<br/>                                                                                        |
| [**Metafile(WCHAR, \* HDC, Rect&,MetaFileFrameUnit,EmfType,WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar))    | Cria um [**objeto Metafile::Metafile**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar)) para gravação.<br/>                                                                                        |
| [**Metafile(WCHAR, \* HDC, RectF&, MetafileFrameUnit,EmfType,WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar))   | Cria um [**objeto Metafile::Metafile**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inconstwchar_inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar)) para gravação.<br/>                                                                                        |
| [**Metafile(IStream, \* HDC, Rect&,MetafileFrameUnit,EmfType,WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar))  | Cria um [**objeto Metafile::Metafile**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inconstrect__inmetafileframeunit_inemftype_inconstwchar)) para gravação em uma interface [IStream.](/windows/win32/api/objidl/nn-objidl-istream)<br/> |
| [**Metafile(IStream, \* HDC, RectF&, MetafileFrameUnit, EmfType,WCHAR \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar)) | Cria um [**objeto Metafile::Metafile**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inistream_inhdc_inconstrectf__inmetafileframeunit_inemftype_inconstwchar)) para gravação em uma interface [IStream.](/windows/win32/api/objidl/nn-objidl-istream)<br/> |



 

 
