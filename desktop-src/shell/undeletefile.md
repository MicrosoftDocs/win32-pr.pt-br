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
ms.openlocfilehash: b7549b521c241429f1c5c7edb7f83eadf25f5d37
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842417"
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

Digite: **HWND**

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



| Código de retorno                                                                             | Descrição                                                        |
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



 

 




