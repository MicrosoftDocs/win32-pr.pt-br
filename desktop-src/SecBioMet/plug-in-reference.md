---
title: Referência de plug-in
description: Funções de adaptador, funções de wrapper e estruturas para criar adaptadores de plug-ins personalizados de três tipos de mecanismo, sensor e armazenamento.
ms.assetid: 1886c389-b914-4b2d-ab7e-3e163782673d
keywords:
- API de Windows Biometric Framework de API de Windows Biometric Framework, referência de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc764be98f6417d211effe1c182279d54c95d234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453711"
---
# <a name="plug-in-reference"></a>Referência de plug-in

Os dispositivos biométricos são fabricados em uma ampla variedade de tipos e configurações. A Windows Biometric Framework incorpora uma arquitetura extensível que permite que você lide com essa variedade criando plug-ins personalizados. No centro dessa arquitetura, há um objeto de software chamado unidade biométrica. Você pode considerar uma unidade biométrica como uma abstração que representa um dispositivo biométrico para a estrutura. Componentes de software de plug-in chamados adaptadores conectam a unidade biométrica ao hardware associado. Há três tipos de adaptadores que você pode criar. Um adaptador de mecanismo gera modelos biométricos de amostras capturadas, corresponde a amostras a modelos existentes e modelos de índices. Um adaptador de sensor encapsula um dispositivo biométrico e fornece uma interface padrão para configurar o sensor, capturar amostras e controlar o fluxo de dados biométricos para o mecanismo de processamento. Um adaptador de armazenamento gerencia bancos de dados de modelo.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                 | Descrição                                                                                                                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Funções de plug-in](plug-in-functions.md)<br/>                 | Funções que você pode usar para criar os plug-ins de adaptador que compõem uma unidade biométrica.<br/>                                                                     |
| [Estruturas de plug-in](plug-in-structures.md)<br/>               | Estruturas para desenvolvimento de aplicativo cliente pela API de Windows Biometric Framework.<br/>                                                                   |
| [Funções de wrapper de plug-in](plug-in-wrapper-functions.md)<br/> | Funções de wrapper que permitem chamar uma função pública em qualquer adaptador anexado ao pipeline sem adquirir manualmente um ponteiro para o adaptador.<br/> |



 

 

 





