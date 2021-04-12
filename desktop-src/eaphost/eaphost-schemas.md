---
title: EAPHost e esquema herdado
description: Descreve o esquema EAPHost e o esquema herdado para criar o XML de configuração e a credencial XML.
ms.assetid: d4572866-7e2b-4e7c-afe1-66394b549bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dbe40f447618a9ca0da89875521349101c1191f
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104365333"
---
# <a name="eaphost-and-legacy-schema"></a>EAPHost e esquema herdado

Este tópico descreve o esquema EAPHost e o esquema herdado para criar o XML de configuração e a credencial XML.

## <a name="about-eaphost-and-legacy-schema"></a>Sobre o EAPHost e o esquema herdado

A criação do XML de configuração começa com o esquema [eaphostconfig](eaphostconfigschema-schema.md) ; a criação de credencial XML começa com o esquema [eaphostusercredentials](eaphostusercredentialsschema-schema.md) .

Vários dos esquemas nativos e herdados contêm elementos de esquema comuns. Os elementos comuns usados na configuração do método e as credenciais do método são dissociados em um único arquivo de esquema, conhecido como "esquema comum".

Os termos "configuração do método" e "Propriedades da conexão" são usados de maneira intercambiável. Da mesma forma, os termos "credenciais do método" e "Propriedades do usuário" também são usados de maneira intercambiável.

## <a name="eaphost-schema"></a>Esquema EAPHost



| Esquema                                                                        | Descrição                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------|
| [baseeapmethodconfig](baseeapmethodconfigschema-schema.md)                   | Contém elementos de esquema de configuração comuns.     |
| [baseeapmethodusercredentials](baseeapmethodusercredentialsschema-schema.md) | Contém elementos de esquema de credencial comuns.        |
| [eapcommon](eapcommonschema-schema.md)                                       | Contém a definição do elemento **EapMethodType** . |
| [eaphostconfig](eaphostconfigschema-schema.md)                               | Contém o esquema de configuração do EAPHost.             |
| [eaphostusercredentials](eaphostusercredentialsschema-schema.md)             | Contém o esquema de credencial EAPHost.                |



 

## <a name="legacy-schema"></a>Esquema herdado



| Esquema                                                                            | Descrição                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)   | Contém elementos de esquema de configuração comuns.                                               |
| [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)               | Contém elementos de esquema de credencial comuns.                                                  |
| [eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)           | Contém elementos de esquema de configuração comuns.                                               |
| [eapuserpropertiesv1](eapuserpropertiesv1schema-schema.md)                       | Contém elementos de esquema de credencial comuns.                                                  |
| [eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)     | É usado com EAP-TLS para descrever os dados de configuração de autenticação.                          |
| [eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-schema.md)     | É usado com EAP-TLS para descrever os dados de configuração de autenticação a partir do Windows 7. |
| [eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)                 | É usado com EAP-TLS para descrever as credenciais de autenticação e as opções de credenciais.          |
| [mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md) | É usado com MS-CHAPv2 para descrever os dados de configuração de autenticação.                        |
| [mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)             | É usado com MS-CHAPv2 para descrever as credenciais de autenticação e as opções de credenciais.        |
| [mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)     | É usado com o PEAPv0 para descrever os dados de configuração de autenticação.                           |
| [mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)     | É usado com o PEAPv0 para descrever os dados de configuração de autenticação que começam com o Windows 7.  |
| [mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)                 | É usado com o PEAPv0 para descrever as credenciais de autenticação e as opções de credenciais.           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Revisão do EAPHost e exemplos de esquema herdados](eaphost-schemas.md)
</dt> </dl>

 

 




