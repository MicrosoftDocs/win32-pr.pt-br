---
description: A interface IX509EndorsementKey expõe as propriedades a seguir.
ms.assetid: 9E93622B-56E9-4F2F-9EFA-4F63D45EDCB6
title: Propriedades IX509EndorsementKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41d135205680e4c998c1157844cfa66a9ef9bd7ef4df5ff8258a31e562a685e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117776184"
---
# <a name="ix509endorsementkey-properties"></a>Propriedades IX509EndorsementKey

A interface [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) expõe as propriedades a seguir.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                        | Descrição                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Propriedade Length**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_length)<br/>             | O comprimento do bit da chave de endosso. Você só poderá acessar essa propriedade depois que [**o método Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) tiver sido chamado.<br/>                                                                                                                                                                                            |
| [**Propriedade aberta**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_opened)<br/>             | Indica se o [**método Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) foi chamado com êxito.<br/>                                                                                                                                                                                                                                            |
| [**Propriedade ProviderName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername)<br/> | O nome do provedor de criptografia. O padrão é o Provedor de Criptografia da Plataforma Microsoft. Você deve definir a [**propriedade ProviderName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) antes de chamar o [**método**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) Open. Não é possível alterar **a propriedade ProviderName** depois de chamar o **método** Open.<br/> |



 

 

 




