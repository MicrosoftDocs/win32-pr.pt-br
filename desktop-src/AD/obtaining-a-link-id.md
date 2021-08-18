---
title: Obtendo uma ID de link
description: A partir do Windows Server 2003, não é mais necessário solicitar uma linkID da Microsoft; há um processo para gerar automaticamente uma linkID.
ms.assetid: e3bf2936-40b1-46b5-8ee9-ab208bb388f6
ms.tgt_platform: multiple
keywords:
- Obtendo uma ID de link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1800448e8cc665e0a28a88800a592e33d7b6ee5a766743d8a681a121c5ad02c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025554"
---
# <a name="obtaining-a-link-id"></a>Obtendo uma ID de link

A partir do Windows Server 2003, não é mais necessário solicitar uma [**linkID**](/windows/desktop/ADSchema/a-linkid) da Microsoft; há um processo para gerar automaticamente uma **linkID.** O sistema gerará automaticamente uma ID de link para um novo atributo vinculado quando o atributo **linkID** do atributo for definido como 1.2.840.113556.1.2.50. Um link de retorno para esse link de encaminhamento é criado definindo a **linkID** como [**attributeID**](/windows/desktop/ADSchema/a-attributeid) ou [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) do link de encaminhamento. O cache de esquema deve ser recarregado depois de criar o link de encaminhamento e antes de criar o link voltar. Caso contrário, **attributeId** ou **ldapDisplayName** do link de encaminhamento não serão encontrados quando o link voltar for criado. O cache de esquema é recarregado sob demanda, alguns minutos depois que uma alteração de esquema é feita ou quando o DC é reiniciado. Crie todos os links de encaminhamento, recarregue o cache de esquema e, em seguida, crie todos os links de retorno.

Por exemplo, quando você criou os novos atributos **myForwardLinkAttr** e **myBackLinkAttr** e deseja vinculá-los:

> [!Note]  
> Os OIDs neste exemplo são artificialmente. Consulte [Obtendo um identificador de objeto da Microsoft para](obtaining-an-object-identifier-from-microsoft.md) obter instruções sobre como obter OIDs para novos atributos.

 

1.  De definir esses atributos no atributo que deve ser o link de encaminhamento:
    ```C++
    ldapDisplayName: myForwardLinkAttr
    OID: 1.2.840.113556.6.1234
    LinkID: 1.2.840.113556.1.2.50
    ```

    

2.  Recarregue o esquema.
3.  De definir esses atributos no atributo que deve ser o link de retorno:
    ```C++
    ldapDisplayName: myBackLinkAttr
    OID: 1.2.840.113556.6.1235
    LinkID: 1.2.840.113556.6.1234 or myForwardLinkAttr
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos vinculados](linked-attributes.md)
</dt> <dt>

[Como estender o esquema](how-to-extend-the-schema.md)
</dt> </dl>

 

 