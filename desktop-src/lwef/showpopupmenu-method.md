---
title: Método ShowPopupMenu
description: Método ShowPopupMenu
ms.assetid: 7f964d53-2594-41b1-9450-1ba7e9f85882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0325a552cc3c1f91a64c1240964f1d0c329292c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813639"
---
# <a name="showpopupmenu-method"></a>Método ShowPopupMenu

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Exibe o menu pop-up do caractere no local especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agente. ***Caracteres ("*** characterid ***"). ShowPopupMenu*** x, y*



| Parte | Descrição                                                                                                                                          |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x*  | Obrigatórios. Um valor inteiro que indica a coordenada de tela horizontal (*x*) para exibir o menu. Essas coordenadas devem ser especificadas em pixels. |
| *y*  | Obrigatórios. Um valor inteiro que indica a coordenada de tela vertical (*y*) para exibir o menu. Essas coordenadas devem ser especificadas em pixels.   |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O Agent exibe automaticamente o menu pop-up do caractere quando o usuário clica com o botão direito do mouse no caractere. Se você definir [**AutoPopupMenu**](autopopupmenu-property.md) como **false**, poderá usar esse método para exibir o menu.

O menu permanece exibido até que o usuário selecione um comando ou exiba outro menu. Somente um menu pop-up pode ser exibido de cada vez; Portanto, as chamadas para esse método irão cancelar (remover) o menu anterior.

Esse método deve ser chamado somente quando o aplicativo cliente é o cliente ativo do caractere; caso contrário, ele falhará. Para determinar o sucesso desse método, você pode chamá-lo como uma função e ele retornará um valor booliano indicando se o método teve êxito.


```
   If Genie.ShowPopupMenu (10,10) = True Then
      ' The menu will be displayed

   Else 
      ' The menu will not be displayed

   End If
```



## <a name="see-also"></a>Consulte Também

[**Propriedade AutoPopupMenu**](autopopupmenu-property.md)


 

 




