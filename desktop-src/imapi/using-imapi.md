---
title: Usando IMAPI
description: Os tópicos a seguir demonstram o uso da API de controle de imagem.
ms.assetid: c42043db-612f-488f-a6ae-a8caea8ac42b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7bf19d619f6ed5ab9a2d6b0deb1ca6a42b71a0b0941a96f54cccfa87c14b5f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092426"
---
# <a name="using-imapi"></a>Usando IMAPI

Os tópicos a seguir demonstram o uso da API de controle de imagem.

## <a name="usage-scenarios"></a>Cenários de uso

A documentação a seguir fornece diretrizes detalhadas para cenários comuns de IMAPI.



| Cenário                                                                                                         | Descrição                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Verificando o suporte à unidade](checking-drive-support.md)                                                             | Demonstra a detecção de suporte para uma unidade de mídia.<br/>                                                                                                   |
| [Verificando o suporte à mídia](checking-media-support.md)                                                             | Demonstra a detecção de suporte para mídia.<br/>                                                                                                           |
| [Gravar uma imagem de disco](burning-a-disc.md)                                                                       | Demonstra o domínio (gravar um disco) usando IMAPI.<br/>                                                                                                       |
| [Adicionando uma imagem de inicialização](adding-a-boot-image.md)                                                                   | Se baseia no exemplo [Gravar uma Imagem de Disco](burning-a-disc.md) adicionando código para incluir uma imagem inicializável na seção de inicialização do disco.<br/>               |
| [Criando um disco de multisessão](creating-a-multisession-disc.md)                                                 | Demonstra a criação de um disco de multisessão usando IMAPI.<br/>                                                                                              |
| [Monitorando o progresso com eventos](monitoring-progress-with-events.md)                                           | Demonstra o uso de interfaces específicas para permitir a implementação de um manipulador de eventos para que informações de progresso possam ser recebidas. <br/>        |
| [Impedindo o logoff ou suspender durante um burn](preventing-logoff-or-suspend-during-a-burn.md)                     | Contém informações que detalham as considerações de desenvolvimento de aplicativos a serem feitas em relação a cenários que envolvem o usuário 'Logoff' e 'Suspend' no Windows.<br/> |
| [Fornecendo permissões de usuário para dispositivos de gravação de mídia](providing-user-permissions-for-media-burning-devices.md) | Detalha o processo necessário para garantir que um usuário tenha permissões adequadas para utilizar dispositivos de gravação de mídia no Windows XP e Windows Server 2003.<br/>             |



 

## <a name="application-compatibility"></a>Compatibilidade de aplicativos

A documentação a seguir contém informações importantes a serem consideradas ao desenvolver um aplicativo que utiliza o IMAPI.



| Diretrizes                                                   | Descrição                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Layout de multisessão IMAPI](imapi-multisession-layout.md) | Detalha o layout do disco que o IMAPI utiliza para implementar a multisessão. Essas informações são usadas para garantir a interoperabilidade entre iMAPI e outros softwares de gravação, bem como permitir a criação de imagens de disco de multisessão compatíveis com IMAPI.<br/> |



 

 

 





