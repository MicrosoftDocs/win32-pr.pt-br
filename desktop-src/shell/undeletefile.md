---
description: Especifica uma função de chamada de retorno definida pelo aplicativo chamada pelo Gerenciador de arquivos quando o usuário escolhe o comando restaurar no menu arquivo.
title: Ponteiro de função FM_UNDELETE_PROC (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_UNDELETE_PROC
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 456b053e-e83d-43af-9691-57e1d4fd3f8f
ms.openlocfilehash: 3bed8995954cdfe05bcc8eea82dc47415033e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171545"
---
# <a name="fm_undelete_proc-function-pointer"></a>\_ \_ Ponteiro da função proc de exclusão de FM

Especifica uma função de chamada de retorno definida pelo aplicativo chamada pelo Gerenciador de arquivos quando o usuário escolhe o comando **restaurar** no menu **arquivo** .

## <a name="syntax"></a>Sintaxe


```C++
typedef DWORD ( APIENTRY *FM_UNDELETE_PROC)(
   HWND  hwndOwner,
   LPSTR lpszDir
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndOwner* 
</dt> <dd>

Tipo: **HWND**

O identificador de janela para o Gerenciador de arquivos. Uma DLL de exclusão deve usar esse identificador para especificar a janela do proprietário de qualquer caixa de diálogo ou caixa de mensagem que a DLL possa exibir.

</dd> <dt>

*lpszDir* 
</dt> <dd>

Tipo: **LPSTR**

O endereço de uma cadeia de caracteres terminada em nulo que contém o nome do diretório inicial.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **DWORD**

Retorna um dos valores a seguir.



| Código de retorno                                                                             | Description                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**-1**</dt> </dl>       | Ocorreu um erro.<br/>                                      |
| <dl> <dt>**IDOK**</dt> </dl>     | Um arquivo não foi excluído. O Gerenciador de arquivos redesenha sua janela.<br/> |
| <dl> <dt>**IDCANCEL**</dt> </dl> | Nenhum arquivo foi reexcluído.<br/>                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



 

 




