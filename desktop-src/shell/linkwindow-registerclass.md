---
description: Registra uma classe de janela que permite que o controle comum SysLink seja usado em uma janela.
ms.assetid: 1e6dd741-81be-40bb-a8b5-d565f593c4e9
title: LinkWindow_RegisterClass função
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_RegisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 75936c918a930698ef803b02743b935660e876b0d87d7f6d5eddce91d4f4c0a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968955"
---
# <a name="linkwindow_registerclass-function"></a>Função LinkWindow \_ RegisterClass

\[Essa função está disponível por meio Windows XP com Service Pack 2 (SP2) e Windows Server 2003. Ele pode ser alterado ou não disponível nas versões subsequentes do Windows. Em vez disso, use [**InitCommonControlsEx.**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex)\]

Registra uma classe de janela que permite que o [controle comum SysLink](../controls/syslink-overview.md) seja usado em uma janela.

## <a name="syntax"></a>Sintaxe


```C++
BOOL LinkWindow_RegisterClass(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **BOOL**

Retornará **TRUE** se o registro tiver sido bem-sucedido; **FALSE caso** contrário, .

## <a name="remarks"></a>Comentários

Essa função não tem um arquivo de biblioteca ou de um header associado, portanto, ela deve ser chamada pelo valor ordinal. Chame [**LoadLibrary com**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o nome da DLL Shell32.dll obter um handle de módulo. Em seguida, [**chame GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com esse alçamento de módulo e o número ordinal 258 para usar essa função.

Use [**LinkWindow \_ UnregisterClass**](linkwindow-unregisterclass.md) para não fazer o registro da classe após o uso.

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

 

 
