---
description: Sobre a arquitetura do ACM
ms.assetid: 4a5c0085-0e7b-424d-9205-5ec39518a088
title: Sobre a arquitetura do ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d75b6b365970c34174facd035ddf38c625e3e4fac72f011e612998c46e9bee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065167"
---
# <a name="about-the-acm-architecture"></a>Sobre a arquitetura do ACM

o módulo de configuração automática (ACM) é o novo componente de configuração sem fio para o Windows Vista. Windows o XP com service pack 3 (SP3) e a API de LAN sem fio para Windows XP com service pack 2 (SP2) usam o serviço WZC (Wireless Zero Configuration).

O ACM verifica as redes periodicamente e usa um processo iterativo para selecionar e se conectar à rede mais preferencial no intervalo, se essa rede tiver uma interface habilitada para conexão automática. O ACM também salva e recupera perfis de rede, que contêm configurações do ACM, módulo específico de mídia (MSM), segurança e fornecedor de hardware independente (IHV). Esses perfis de rede são para configuração automática.

A configuração automática dá suporte a configurações globais e por interface e perfis de rede. As configurações globais e os perfis de rede são configurados se o computador tiver ingressado em um domínio com um GPO (objeto de política de grupo) no nível de domínio ou no nível da UO (unidade organizacional) na hierarquia do Active Directory (AD). Essas configurações e perfis de diretiva de grupo são somente leitura, aplicadas a cada interface 802,11 no sistema e sempre têm precedência sobre as configurações por interface e por usuário e os perfis de rede. Os perfis de política de grupo são colocados na parte superior da lista de perfil de rede preferencial em cada adaptador de rede 802,11.

A arquitetura ACM é extensível. Os IHVs podem implementar a funcionalidade sem fio proprietária sem alterar a estrutura nativa 802,11 fornecida. As funções e estruturas de controle de IHV expostas habilitam essa extensibilidade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre WiFi nativo](about-native-wifi.md)
</dt> </dl>

 

 



