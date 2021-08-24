---
title: Referência da API EAPHost
description: Saiba mais sobre as APIs do EAPHost e seus componentes. Consulte informações de referência para vários tópicos de API, como o esquema XML do EAPHost.
ms.assetid: ac2f074f-b525-42a2-8637-c96a08d77714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c522698999bcb58b4e33b8e1cb0d1bb74ae64fc3b709ce672b35e7db81e85ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739096"
---
# <a name="eaphost-api-reference"></a>Referência da API EAPHost

As APIs do EAPHost são divididas em três componentes: as APIs do suplicante, que podem ser chamadas diretamente de um aplicativo habilitado para EAP; as APIs do método EAP peer, que gerenciam solicitações suplicantes para um tipo de autenticação EAP específico e geram elementos interativos no cliente; e as APIS do autenticador EAP, que executam a autenticação do lado do servidor de um suplicante.

os dois últimos componentes de API – o método eap Peer e as APIs do método eap Authenticator – exigem implementação personalizada e compatível em DLLs que os expõem ao serviço EAPHost. Eles não podem ser chamados diretamente do código do aplicativo; em vez disso, eles são chamados pelo EAPHost (no lado do cliente para métodos de ponto EAP e no lado do servidor para métodos de autenticador EAP) se a implementação corresponder às assinaturas de API especificadas na documentação correspondente. Informações específicas de implementação de API são fornecidas em cada página de referência de função.

## <a name="eaphost-registry-settings"></a>Configurações de registro do EAPHost



| Tópico                                                      | Descrição                                      |
|------------------------------------------------------------|--------------------------------------------------|
| [Configurações de registro do EAPHost](eaphost-registry-settings.md) | Descreve as chaves do registro consumidas pelo EAPHost. |



 

## <a name="eaphost-xml-schema"></a>Esquema XML do EAPHost



| Tópico                                            | Descrição                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [EAPHost e esquema herdado](eaphost-schemas.md) | Descreve o esquema EAPHost e o esquema herdado para criar o XML de configuração e a credencial XML. |



 

## <a name="common-eaphost-api-reference"></a>Referência de API do EAPHost comum



| Tópico                                                                   | Descrição                                  |
|-------------------------------------------------------------------------|----------------------------------------------|
| [Enumerações comuns da API EAPHost](common-eap-host-api-enumerations.md) | Lista as constantes comuns a todas as APIs do EAPHost.  |
| [Estruturas comuns de API do EAPHost](common-eap-host-api-structures.md)     | Lista estruturas comuns a todas as APIs do EAPHost. |
| [Constantes comuns da API EAPHost](common-eap-host-error-constants.md)     | Lista as constantes comuns a todas as APIs do EAPHost.  |



 

## <a name="eaphost-api-reference"></a>Referência da API EAPHost



| Tópico                                                                       | Descrição                                                                                                                                      |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Referência de API do suplicante EAPHost](eap-host-supplicant-api-reference.md)   | Descreve os elementos de API disponíveis para habilitar chamadas de suplicante para EAPHost.                                                                      |
| [Referência da API do método par do EAPHost](eap-host-peer-method-api-reference.md) | Descreve os elementos de API que devem ser implementados para criar uma DLL de método EAP peer que pode ser carregada e chamada por um cliente EAPHost.          |
| [Authenticator de APIs do método EAPHost](eaphost-authenticator-method-apis.md)  | Descreve os elementos de API que devem ser implementados para criar uma DLL de método de autenticador EAP que pode ser carregada e chamada por um servidor EAPHost. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o EAPHost](about-eap-host.md)
</dt> <dt>

[Usando o EAPHost](using-eap-host.md)
</dt> </dl>

 

 




