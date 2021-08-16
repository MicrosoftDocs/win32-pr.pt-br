---
title: IAgentCharacter Show
description: IAgentCharacter Show
ms.assetid: 5f13dcef-3777-41eb-827f-6162bad71a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcefb523bd2e9f477991bf6fa8352382f75b6bc76d93aab2e7f5c9e8cc1358dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692998"
---
# <a name="iagentcharactershow"></a>IAgentCharacter::Show

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

Mostrando o sinalizador de animação de estado. Se esse parâmetro for **True**, a **animação de** estado Mostrando será reproduzível depois de tornar o caractere visível; se **False**, a animação não será reproduzida.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Endereço de uma variável que recebe a ID [**mostrar**](/windows/desktop/lwef/iagentcharacter--show) solicitação.

</dd> </dl>

Evite definir o *parâmetro bFast* como **True** sem exibir uma animação com antecedência; caso contrário, o quadro de caracteres poderá ser exibido, mas não terá nenhuma imagem a ser exibida. Em particular, observe que, se você chamar [**MoveTo**](iagentcharacter--moveto.md) quando o caractere não estiver visível, ele não reproduzirá nenhuma animação. Portanto, se você chamar o **método Show** com *bFast* definido como **True,** nenhuma imagem será exibida. Da mesma forma, se você chamar [**Ocultar**](/windows/desktop/lwef/iagentcharacter--hide)e **Mostrar com** *bFast* definido como **True,** não haverá nenhuma imagem visível.

Ao usar o protocolo HTTP para acessar caracteres e dados de animação, use o método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantir a disponibilidade da animação de **estado** Mostrando antes de chamar esse método.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter::Hide**](iagentcharacter--hide.md)


 

 