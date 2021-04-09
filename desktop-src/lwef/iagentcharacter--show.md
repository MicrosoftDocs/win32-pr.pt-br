---
title: IAgentCharacter mostrar
description: IAgentCharacter mostrar
ms.assetid: 5f13dcef-3777-41eb-827f-6162bad71a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 997a9879d564644085bd92e4515460c3dde33208
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007551"
---
# <a name="iagentcharactershow"></a>IAgentCharacter:: mostrar

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Show(
   long bFast,      // play Showing state animation flag
   long * pdwReqID  // address of request ID
);
```

Exibe um caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida. Quando a função retorna, *pdwReqID* contém a ID da solicitação.

<dl> <dt>

<span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*
</dt> <dd>

Sinalizador de animação de estado de exibição. Se esse parâmetro for **true**, a animação de estado de **exibição** será reproduzida depois de tornar o caractere visível; Se **for false**, a animação não será reproduzida.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Endereço de uma variável que recebe a ID da solicitação de [**exibição**](/windows/desktop/lwef/iagentcharacter--show) .

</dd> </dl>

Evite definir o parâmetro *bFast* como **true** sem reproduzir uma animação com antecedência. caso contrário, o quadro de caracteres poderá ser exibido, mas não terá nenhuma imagem a ser exibida. Em particular, observe que, se você chamar [**MoveTo**](iagentcharacter--moveto.md) quando o caractere não estiver visível, ele não reproduzirá nenhuma animação. Portanto, se você chamar o método **show** com *BFast* definido como **true**, nenhuma imagem será exibida. Da mesma forma, se você chamar [**ocultar**](/windows/desktop/lwef/iagentcharacter--hide)e, em seguida, **Mostrar** com *bFast* definido como **true**, não haverá imagem visível.

Ao usar o protocolo HTTP para acessar dados de caracteres e animações, use o método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantir a disponibilidade da animação de estado **mostrando** antes de chamar esse método.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter:: Hide**](iagentcharacter--hide.md)


 

 