---
title: Usando o IMAPi
description: Os tópicos a seguir demonstram o uso da API de mestre de imagem.
ms.assetid: c42043db-612f-488f-a6ae-a8caea8ac42b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccd44d01e925d07d251e93a29c5268cc7e9c5076
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823034"
---
# <a name="using-imapi"></a>Usando o IMAPi

Os tópicos a seguir demonstram o uso da API de mestre de imagem.

## <a name="usage-scenarios"></a>Cenários de uso

A documentação a seguir fornece orientações detalhadas para cenários comuns de IMAPi.



| Cenário                                                                                                         | Descrição                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Verificando o suporte à unidade](checking-drive-support.md)                                                             | Demonstra a detecção de suporte para uma unidade de mídia.<br/>                                                                                                   |
| [Verificando o suporte de mídia](checking-media-support.md)                                                             | Demonstra a detecção de suporte para mídia.<br/>                                                                                                           |
| [Gravando uma imagem de disco](burning-a-disc.md)                                                                       | Demonstra como dominar (gravar um disco) usando o IMAPi.<br/>                                                                                                       |
| [Adicionando uma imagem de inicialização](adding-a-boot-image.md)                                                                   | Baseia-se no exemplo de [gravação de uma imagem de disco](burning-a-disc.md) adicionando código para incluir uma imagem inicializável na seção de inicialização do disco.<br/>               |
| [Criando um disco de várias sessões](creating-a-multisession-disc.md)                                                 | Demonstra a criação de um disco de várias sessões usando IMAPi.<br/>                                                                                              |
| [Progresso do monitoramento com eventos](monitoring-progress-with-events.md)                                           | Demonstra o uso de interfaces específicas para permitir a implementação de um manipulador de eventos para que as informações de progresso possam ser recebidas. <br/>        |
| [Impedindo o logoff ou a suspensão durante uma gravação](preventing-logoff-or-suspend-during-a-burn.md)                     | Contém informações detalhadas sobre o desenvolvimento de aplicativos que devem ser feitas em relação a cenários envolvendo o usuário ' logoff ' e ' suspender ' no Windows.<br/> |
| [Fornecendo permissões de usuário para dispositivos de gravação de mídia](providing-user-permissions-for-media-burning-devices.md) | Detalha o processo necessário para garantir que um usuário tenha as permissões adequadas para utilizar dispositivos de gravação de mídia no Windows XP e no Windows Server 2003.<br/>             |



 

## <a name="application-compatibility"></a>Compatibilidade de aplicativos

A documentação a seguir contém informações importantes a serem levadas em consideração ao desenvolver um aplicativo que utiliza o IMAPi.



| Diretrizes                                                   | Descrição                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Layout de várias sessões do IMAPi](imapi-multisession-layout.md) | Detalha o layout do disco que o IMAPi utiliza para implementar várias sessões. Essas informações são usadas para garantir a interoperabilidade entre o IMAPi e outros softwares de gravação, além de permitir a criação de imagens de disco de várias sessões compatíveis com o IMAPi.<br/> |



 

 

 





