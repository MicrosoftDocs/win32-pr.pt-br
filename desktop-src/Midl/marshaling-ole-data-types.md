---
title: Empacotamento de tipos de dados OLE
description: Marshaling de automação e tipos de dados OLE.
ms.assetid: 0cab4208-d40d-40a1-88f2-4933b52c0c29
keywords:
- MIDL e MIDL de COM, marshaling de tipos de dados OLE
- empacotamento de MIDL
- MIDL de dados OLE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5970c6e0fef9d0fc88b8a0a11a087fa4396d7a7c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640563"
---
# <a name="marshaling-ole-data-types"></a>Empacotamento de tipos de dados OLE

Para facilitar o uso de determinados tipos de dados OLE e de automação, bem como alguns identificadores de sistema frequentemente usados em COM, typedefs para esses tipos de dados e suas funções auxiliares relacionadas estão disponíveis Importando arquivos IDL do Windows e vinculando aos arquivos DLL OLE e Automation. Esses arquivos são instalados automaticamente no seu sistema.

-   Para usar o tipo de dados [**BSTR**](/previous-versions/windows/desktop/automat/bstr) em chamadas de procedimento remoto, importe o arquivo wtypes. idl para seu arquivo de definição de interface (IDL) e vincule a Oleaut32. lib ao compilar seu aplicativo distribuído. Isso permitirá que seus stubs usem as funções auxiliares **BSTR \_ nosize**, **BSTR \_ usermarshal**, **BSTR \_ UserUnmarshal** e **BSTR \_ unfree**.
-   Para usar outros tipos de dados de automação, como [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) e [**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray), ou tipos que usam esses tipos (por exemplo, [**DISPPARAMS**](/windows/win32/api/oaidl/ns-oaidl-dispparams) e [**EXCEPINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo)), importe o arquivo Objidl. idl para o arquivo IDL e vincule ao Oleaut32. lib no momento da compilação. Isso permitirá que você use as rotinas apropriadas do auxiliar.
-   Para usar tipos de dados OLE (como CLIPFORMAT, SNB, STGMEDIUM, ASYNC \_ STGMEDIUM) ou identificadores do sistema (como HMETAFILE \_ PICT, HENHMETAFILE, HMETAFILE, HBITMAP, HPALETTE e HGLOBAL), importe o arquivo Objidl. idl para o arquivo de definição de interface e vincule ao Ole32. lib no momento da compilação.
-   Os seguintes identificadores OLE também são definidos com o atributo de **\[ \_ marshaling \] de fio** , mas somente como identificadores em um computador, pois não podem ser usados em chamadas de procedimento remoto para outros computadores neste momento: HWND, HMENU, HACCEL, HDC, HFONT, hicon, HBRUSH. Importe o arquivo Objidl. idl para o arquivo IDL e vincule a Ole32. lib no momento da compilação para usar esses identificadores na comunicação entre processos em um único computador.

Para obter mais informações, consulte [o \_ atributo de marshaling de fio](/windows/desktop/Rpc/the-wire-marshal-attribute), [a \_ função Usersize](/windows/desktop/Rpc/the-type-usersize-function), [o tipo \_ função usermarshal](/windows/desktop/Rpc/the-type-usermarshal-function), [o tipo \_ UserUnmarshal function](/windows/desktop/Rpc/the-type-userunmarshal-function), [o tipo \_ usergratuito function](/windows/desktop/Rpc/the-type-userfree-function)e [direcionando stubs para plataformas específicas de 32 bits ou 64 bits](targeting-stubs-for-specific-32-bit-or-64-bit-platforms.md).

 

 