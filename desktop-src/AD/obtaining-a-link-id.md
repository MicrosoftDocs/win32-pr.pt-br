---
title: Obtendo uma ID de link
description: A partir do Windows Server 2003, não é mais necessário solicitar uma LinkId da Microsoft; Há um processo para gerar automaticamente um LinkID.
ms.assetid: e3bf2936-40b1-46b5-8ee9-ab208bb388f6
ms.tgt_platform: multiple
keywords:
- Obtendo uma ID de link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6893baab780d7fb481de0af77a607e988c3f87a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084443"
---
# <a name="obtaining-a-link-id"></a>Obtendo uma ID de link

A partir do Windows Server 2003, não é mais necessário solicitar uma [**LinkId**](/windows/desktop/ADSchema/a-linkid) da Microsoft; Há um processo para gerar automaticamente um **LinkId**. O sistema irá gerar automaticamente uma ID de link para um novo atributo vinculado quando o atributo **LinkId** do atributo for definido como 1.2.840.113556.1.2.50. Um link regressivo para esse link de encaminhamento é criado definindo o **LinkId** para o [**AttributeID**](/windows/desktop/ADSchema/a-attributeid) ou o [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) do link de encaminhamento. O cache de esquema deve ser recarregado após a criação do link de encaminhamento e antes da criação do link voltar. Caso contrário, o **AttributeID** ou **ldapDisplayName** do link de encaminhamento não será encontrado quando o link voltar for criado. O cache de esquema é recarregado sob demanda, alguns minutos depois que uma alteração de esquema é feita ou quando o DC é reiniciado. Crie todos os links de encaminhamento, recarregue o cache de esquema e, em seguida, crie todos os links de volta.

Por exemplo, quando você criou os novos atributos **myForwardLinkAttr** e **myBackLinkAttr**, e deseja vinculá-los:

> [!Note]  
> Os OIDs neste exemplo são forçado. Consulte [obtendo um identificador de objeto da Microsoft](obtaining-an-object-identifier-from-microsoft.md) para obter instruções sobre como obter OIDs para novos atributos.

 

1.  Defina esses atributos no atributo que deve ser o link de encaminhamento:
    ```C++
    ldapDisplayName: myForwardLinkAttr
    OID: 1.2.840.113556.6.1234
    LinkID: 1.2.840.113556.1.2.50
    ```

    

2.  Recarregue o esquema.
3.  Defina esses atributos no atributo que será o link voltar:
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

 

 