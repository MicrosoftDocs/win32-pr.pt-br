---
description: A interface IX509EndorsementKey expõe as propriedades a seguir.
ms.assetid: 9E93622B-56E9-4F2F-9EFA-4F63D45EDCB6
title: Propriedades de IX509EndorsementKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4bbdbc464803988f5b1100ac42fc0e3697fb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749476"
---
# <a name="ix509endorsementkey-properties"></a>Propriedades de IX509EndorsementKey

A interface [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) expõe as propriedades a seguir.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                        | Descrição                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Propriedade Length**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_length)<br/>             | O comprimento de bit da chave de endosso. Você só pode acessar essa propriedade depois que o método [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) tiver sido chamado.<br/>                                                                                                                                                                                            |
| [**Propriedade aberta**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_opened)<br/>             | Indica se o método [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) foi chamado com êxito.<br/>                                                                                                                                                                                                                                            |
| [**Propriedade ProviderName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername)<br/> | O nome do provedor de criptografia. O padrão é o provedor Microsoft Platform crypto. Você deve definir a propriedade [**ProviderName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) antes de chamar o método [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) . Você não pode alterar a propriedade **ProviderName** depois de ter chamado o método **Open** .<br/> |



 

 

 




