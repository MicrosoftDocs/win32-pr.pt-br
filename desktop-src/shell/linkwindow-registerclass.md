---
description: Registra uma classe de janela que permite que o controle comum SysLink seja usado em uma janela.
ms.assetid: 1e6dd741-81be-40bb-a8b5-d565f593c4e9
title: Função LinkWindow_RegisterClass
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
ms.openlocfilehash: 7b5bfd2e1a45ff3f65df7cf3d3cae41bf4926aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968018"
---
# <a name="linkwindow_registerclass-function"></a>\_Função registerClass LinkWindow

\[Essa função está disponível por meio do Windows XP com Service Pack 2 (SP2) e Windows Server 2003. Ele pode ser alterado ou indisponível nas versões subsequentes do Windows. Use [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) em vez disso.\]

Registra uma classe de janela que permite que o controle comum [Syslink](../controls/syslink-overview.md) seja usado em uma janela.

## <a name="syntax"></a>Sintaxe


```C++
BOOL LinkWindow_RegisterClass(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **bool**

Retornará **true** se o registro tiver sido bem-sucedido; Caso contrário, **false** .

## <a name="remarks"></a>Comentários

Essa função não tem um cabeçalho ou arquivo de biblioteca associado, portanto, ele deve ser chamado pelo valor ordinal. Chame [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) com o nome da dll Shell32.dll para obter um identificador de módulo. Em seguida, chame [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) com esse identificador de módulo e o número ordinal 258 para usar essa função.

Use [**LinkWindow \_ UnregisterClass**](linkwindow-unregisterclass.md) para cancelar o registro da classe após o uso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral dos controles SysLink](../controls/syslink-overview.md)
</dt> </dl>

 

 
