---
description: SFVM \_ GETDETAILSOF pode ser alterado ou indisponível.
ms.assetid: 46a81a7b-527c-4d41-8d25-ce65fd87416e
title: Mensagem de SFVM_GETDETAILSOF (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6170c0fc8dc29435b2c6f2bb033f30706ccb7b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968067"
---
# <a name="sfvm_getdetailsof-message"></a>\_Mensagem SFVM GETDETAILSOF

\[**SFVM \_ O GETDETAILSOF** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

Permite que o objeto de retorno de chamada forneça os detalhes de um item em uma pasta do Shell. Use somente se uma chamada para [**IShellFolder2:: GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) falhar e não houver nenhum método [**IShellDetails:: GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) disponível para chamar. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETDETAILSOF
    wParam = (WPARAM)(int) iColumn;
    lParam = (LPARAM)(DETAILSINFO*) pDi;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IColumn* \[ no\]
</dt> <dd>

A ID de base zero da coluna.

</dd> <dt>

*pDi* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura [**DETAILSINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) preenchida com as informações solicitadas.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                |
| Fim do suporte do cliente<br/>    | Windows XP com SP2<br/>                                                      |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
