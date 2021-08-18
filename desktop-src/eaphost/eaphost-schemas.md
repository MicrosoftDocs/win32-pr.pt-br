---
title: EAPHost e esquema herdado
description: Descreve o esquema EAPHost e o esquema herdado para criar XML de configuração e XML de credencial.
ms.assetid: d4572866-7e2b-4e7c-afe1-66394b549bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4eb9f09a0f1380ad0373ec1171b0b0ea9101af87335d25287969d9a5f7f2da9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984226"
---
# <a name="eaphost-and-legacy-schema"></a>EAPHost e esquema herdado

Este tópico descreve o esquema EAPHost e o esquema herdado para criar XML de configuração e XML de credencial.

## <a name="about-eaphost-and-legacy-schema"></a>Sobre o EAPHost e o esquema herdado

A criação de XML de configuração começa com [o esquema eaphostconfig;](eaphostconfigschema-schema.md) A criação de XML de credencial começa [com o esquema eaphostusercredentials.](eaphostusercredentialsschema-schema.md)

Vários dos esquemas nativos e herdados contêm elementos de esquema comuns. Elementos comuns usados na configuração de método e credenciais de método são abstraídos em um único arquivo de esquema, conhecido como "esquema comum".

Os termos "configuração de método" e "propriedades de conexão" são usados de forma intercambiável. Da mesma forma, os termos "credenciais de método" e "propriedades do usuário" também são usados de forma intercambiável.

## <a name="eaphost-schema"></a>Esquema EAPHost



| Esquema                                                                        | Descrição                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------|
| [baseeapmethodconfig](baseeapmethodconfigschema-schema.md)                   | Contém elementos comuns de esquema de configuração.     |
| [baseeapmethethethercredentials](baseeapmethodusercredentialsschema-schema.md) | Contém elementos comuns de esquema de credencial.        |
| [eapcommon](eapcommonschema-schema.md)                                       | Contém a **definição de elemento EapMethodType.** |
| [eaphostconfig](eaphostconfigschema-schema.md)                               | Contém o esquema de configuração do EAPHost.             |
| [eaphostusercredentials](eaphostusercredentialsschema-schema.md)             | Contém o esquema de credencial EAPHost.                |



 

## <a name="legacy-schema"></a>Esquema herdado



| Esquema                                                                            | Descrição                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)   | Contém elementos comuns de esquema de configuração.                                               |
| [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)               | Contém elementos comuns de esquema de credencial.                                                  |
| [eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)           | Contém elementos comuns de esquema de configuração.                                               |
| [eapuserpropertiesv1](eapuserpropertiesv1schema-schema.md)                       | Contém elementos comuns de esquema de credencial.                                                  |
| [eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)     | É usado com EAP-TLS para descrever dados de configuração de autenticação.                          |
| [eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-schema.md)     | É usado com EAP-TLS para descrever dados de configuração de autenticação que começam com Windows 7. |
| [eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)                 | É usado com EAP-TLS para descrever as credenciais de autenticação e as opções de credencial.          |
| [mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md) | É usado com o MS-CHAPv2 para descrever dados de configuração de autenticação.                        |
| [mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)             | É usado com o MS-CHAPv2 para descrever as credenciais de autenticação e as opções de credenciais.        |
| [mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)     | É usado com PEAPv0 para descrever dados de configuração de autenticação.                           |
| [mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)     | É usado com PEAPv0 para descrever dados de configuração de autenticação que começam com Windows 7.  |
| [mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)                 | É usado com PEAPv0 para descrever as credenciais de autenticação e as opções de credenciais.           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Revendo exemplos de esquema herdado e EAPHost](eaphost-schemas.md)
</dt> </dl>

 

 




