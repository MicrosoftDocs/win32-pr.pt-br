---
description: 'Permite que o objeto de retorno de chamada especifique que uma animação seja exibida enquanto os itens são enumerados em um thread em segundo plano. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: 6f8b3894-f08f-4ebf-a645-87869e7d1b20
title: Mensagem de SFVM_GETANIMATION (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e4281689556e8315da7a9550fd69acc1a327a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091771"
---
# <a name="sfvm_getanimation-message"></a>\_Mensagem GETanimation do SFVM

Permite que o objeto de retorno de chamada especifique que uma animação seja exibida enquanto os itens são enumerados em um thread em segundo plano. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETANIMATION 

    wParam = (WPARAM)(HINSTANCE*) phinst;

    lParam = (LPARAM)(WCHAR*) pwszName;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*phinst* \[ fora\]
</dt> <dd>

O identificador de instância do módulo do qual o recurso deve ser carregado.

</dd> <dt>

*pwszName* \[ fora\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o caminho do arquivo. avi ou o nome de um recurso AVI. Como alternativa, esse parâmetro pode consistir no identificador de recurso na palavra de ordem inferior e 0 na palavra de ordem superior. Para criar esse valor, use a macro [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) . O controle carrega o recurso do módulo especificado por hinst. Um recurso AVI deve ter o tipo "AVI".

</dd> </dl>

## <a name="remarks"></a>Comentários

Por padrão, o objeto de exibição de pasta do sistema exibe a animação "lanterna" durante uma enumeração em segundo plano.

*phinst* e *pwszName* serão passados para o [controle de animação](../controls/animation-control-overview.md) com uma [**mensagem \_ aberta do ACM**](../controls/acm-open.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
