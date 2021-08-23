---
title: Método ShowPopupMenu
description: Método ShowPopupMenu
ms.assetid: 7f964d53-2594-41b1-9450-1ba7e9f85882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0cfd080adcf0158a628f019b4d48be5cd10b9c5b47d7a4b71ccd2393ad83ce6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600986"
---
# <a name="showpopupmenu-method"></a>Método ShowPopupMenu

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Exibe o menu pop-up do caractere no local especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). ShowPopupMenu_ * _x, y_



| Parte | Descrição                                                                                                                                          |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x*  | Obrigatórios. Um valor inteiro que indica a coordenada de tela horizontal (*x*) para exibir o menu. Essas coordenadas devem ser especificadas em pixels. |
| *y*  | Obrigatórios. Um valor inteiro que indica a coordenada de tela vertical (*y*) para exibir o menu. Essas coordenadas devem ser especificadas em pixels.   |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O Agent exibe automaticamente o menu pop-up do caractere quando o usuário clica com o botão direito do mouse no caractere. Se você definir [**AutoPopupMenu**](autopopupmenu-property.md) como **False,** poderá usar esse método para exibir o menu.

O menu permanece exibido até que o usuário selecione um comando ou exibe outro menu. Somente um menu pop-up pode ser exibido por vez; portanto, as chamadas para esse método cancelarão (removerão) o menu anterior.

Esse método deve ser chamado somente quando o aplicativo cliente for o cliente ativo do caractere; caso contrário, falhará. Para determinar o sucesso desse método, você pode chamá-lo como uma função e ele retornará um valor booliana que indica se o método foi bem-sucedido.


```
   If Genie.ShowPopupMenu (10,10) = True Then
      ' The menu will be displayed

   Else 
      ' The menu will not be displayed

   End If
```



## <a name="see-also"></a>Consulte Também

[**Propriedade AutoPopupMenu**](autopopupmenu-property.md)


 

 




