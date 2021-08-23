---
description: Registra uma classe de janela registrada por LinkWindow \_ RegisterClass.
ms.assetid: 9e5c4326-efd1-43ca-a087-a436fe3f9bbd
title: LinkWindow_UnregisterClass função
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_UnregisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 05a50d5f3af72c31ee04a1a9e8264acb22327c38f79f765ce2ad7a740086747e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968935"
---
# <a name="linkwindow_unregisterclass-function"></a>Função LinkWindow \_ UnregisterClass

\[Essa função está disponível por meio Windows XP com Service Pack 2 (SP2) e Windows Server 2003. Ele pode ser alterado ou não disponível nas versões subsequentes do Windows.\]

Registra uma classe de janela registrada por [**LinkWindow \_ RegisterClass**](linkwindow-registerclass.md).

## <a name="syntax"></a>Sintaxe


```C++
BOOL LinkWindow_UnregisterClass(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **BOOL**

Retornará **TRUE** se a operação tiver sido bem-sucedida; **FALSE caso** contrário, .

## <a name="remarks"></a>Comentários

Essa função não tem um arquivo de biblioteca ou de um header associado, portanto, ela deve ser chamada pelo valor ordinal. Chame [**LoadLibrary com**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o nome da DLL Shell32.dll obter um handle de módulo. Em seguida, [**chame GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com esse alçamento de módulo e o número ordinal 259 para usar essa função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral dos controles SysLink](../controls/syslink-overview.md)
</dt> </dl>

 

 
