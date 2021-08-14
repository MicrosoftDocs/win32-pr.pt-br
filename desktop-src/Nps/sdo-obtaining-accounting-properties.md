---
title: Obtendo propriedades de contabilidade
description: O objeto de contabilidade é um dos objetos na coleção de manipuladores de solicitação.
ms.assetid: eb5c8606-d3f0-4c33-9035-7b7b1369cb0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77390a6aa67e946de6d69dd3d1bc28a76907b7ad31b497d4921c7a2d7493c328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361724"
---
# <a name="obtaining-accounting-properties"></a>Obtendo propriedades de contabilidade

> [!Note]  
> o IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008. O conteúdo deste tópico aplica-se ao IAS e ao NPS. Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.

 

O objeto de contabilidade é um dos objetos na coleção de manipuladores de solicitação. O valor de enumeração para a coleção de manipuladores de solicitação é a **propriedade \_ REQUESTHANDLERS do IAS \_ \_**. O nome do manipulador para o objeto de contabilidade é "Microsoft Accounting".

o código de Visual Basic a seguir acessa as propriedades disponíveis do manipulador de objeto de contabilidade.


```VB
Set sdoRequestHandler = sdoCollRequestHandlers.Item("Microsoft Accounting")
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING_INTERIM)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_AUTHENTICATION)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_FILE_DIRECTORY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_IAS1_FORMAT)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE)
```



Para acessar as propriedades de contabilidade usando C++, primeiro obtenha a coleção de manipuladores de solicitação. A [recuperação de uma coleção contém um](/windows/desktop/Nps/sdo-retrieving-a-collection) código C++ que demonstra como obter uma coleção. O valor de enumeração para a coleção de manipuladores de solicitação é a **propriedade \_ REQUESTHANDLERS do IAS \_ \_**. (Os valores correspondentes às várias coleções de NPS são enumerados pelo tipo de enumeração [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) .)

A coleção de manipuladores de solicitação contém um objeto chamado "Microsoft Accounting". Recupere este objeto da coleção. A seção [recuperando um objeto de uma coleção](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) contém um código C++ que demonstra como obter um objeto de uma coleção.

Depois que você tiver o objeto Microsoft Accounting, obtenha uma interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) para o objeto usando [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). A seção [recuperando um usuário SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contém um código C++ que demonstra como obter uma interface **ISdo** para um objeto. Em seguida, você pode usar o método [**ISdo:: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) para obter valores de propriedade para o objeto Microsoft Accounting.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recuperando uma coleção](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[Recuperando um objeto de uma coleção](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection)
</dt> <dt>

[Recuperando um SDO de usuário](/windows/desktop/Nps/sdo-retrieving-a-user-sdo)
</dt> <dt>

[**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> <dt>

[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 