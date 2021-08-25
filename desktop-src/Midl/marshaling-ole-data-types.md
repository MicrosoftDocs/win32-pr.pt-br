---
title: Marshaling de tipos de dados OLE
description: Marshaling de automação e tipos de dados OLE.
ms.assetid: 0cab4208-d40d-40a1-88f2-4933b52c0c29
keywords:
- MIDL e COM MIDL , marshaling de tipos de dados OLE
- marshaling de MIDL
- MIDL de dados OLE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91c5f1527ffaa361b85550941af1538c99251e59750b27f3bfe7552251e821e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895016"
---
# <a name="marshaling-ole-data-types"></a>Marshaling de tipos de dados OLE

Para facilitar o uso de determinados tipos de dados de Automação e OLE, bem como alguns identificadores de sistema usados com frequência no COM, os typedefs para esses tipos de dados e suas funções auxiliares relacionadas estão disponíveis importando arquivos IDL do Windows e vinculando-se aos arquivos OLE e DLL de Automação. Esses arquivos são instalados automaticamente em seu sistema.

-   Para usar o tipo de dados [**BSTR**](/previous-versions/windows/desktop/automat/bstr) em chamadas de procedimento remoto, importe o arquivo wtypes.idl para o arquivo de IDL (definição de interface) e vincule ao Oleaut32.lib ao criar seu aplicativo distribuído. Isso permitirá que seus stubs usem as funções auxiliares **prontas BSTR \_ UserSize,** **BSTR \_ UserMarshal,** **BSTR \_ UserUnmarshal** e **BSTR \_ UserFree.**
-   Para usar outros tipos de dados de Automação, como [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) e [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray)ou tipos que usam esses tipos (por exemplo, [**DISPPARAMS**](/windows/win32/api/oaidl/ns-oaidl-dispparams) e [**EXCEPINFO),**](/windows/win32/api/oaidl/ns-oaidl-excepinfo)importe o arquivo objidl.idl para o arquivo IDL e vincule ao oleaut32.lib no momento do build. Isso permitirá que você use as rotinas auxiliares apropriadas.
-   Para usar tipos de dados OLE (como CLIPFORMAT, SNB, STGMEDIUM, ASYNC STGMEDIUM) ou identificador de sistema \_ (como HMETAFILE \_ PICT, HENCRONAFILE, HMETAFILE, HBITMAP, HPALETTE e HGLOBAL), importe o arquivo objidl.idl para o arquivo de definição de interface e vincule ao ole32.lib no momento do build.
-   Os seguintes handles OLE também são definidos com o atributo **\[ wire \_ \] marshal,** mas apenas como alças em um computador, pois eles não podem ser usados em chamadas de procedimento remoto para outros computadores no momento: HWND, HMENU, HACCEL, HDC, HFONT, HICON, HBRUSH. Importe o arquivo objidl.idl para o arquivo IDL e vincule-o ao ole32.lib no momento da computação para usar esses handles na comunicação entre processos em um único computador.

Para obter mais informações, consulte O atributo wire [ \_ marshal](/windows/desktop/Rpc/the-wire-marshal-attribute), o tipo [Função \_ UserSize](/windows/desktop/Rpc/the-type-usersize-function), o tipo [Função \_ UserMarshal](/windows/desktop/Rpc/the-type-usermarshal-function), o tipo [Função \_ UserUnmarshal](/windows/desktop/Rpc/the-type-userunmarshal-function), o tipo [Função \_ UserFree](/windows/desktop/Rpc/the-type-userfree-function)e Stubs de direcionamento para [plataformas específicas de 32 ou 64](targeting-stubs-for-specific-32-bit-or-64-bit-platforms.md)bits.

 

 