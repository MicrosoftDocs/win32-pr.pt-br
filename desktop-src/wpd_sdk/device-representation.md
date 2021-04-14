---
description: Representação do dispositivo
ms.assetid: bf8b9c67-b023-40ed-97c6-9ca030de610a
title: Representação do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c95352c191d3e2d34392f4236b926b81cf65fd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461064"
---
# <a name="device-representation"></a>Representação do dispositivo

Os dispositivos têm dois comportamentos principais que são abordados pela arquitetura de dispositivos portáteis do Windows (WPD):

-   Acessando e armazenando conteúdo. Por exemplo, os aplicativos devem ser capazes de adicionar arquivos de música a um player portátil de música.
-   Programando o dispositivo. Isso inclui operações simples, como alteração de configurações e preparação do dispositivo para captura de dados, ou operações mais complexas, como carregar o firmware. Os exemplos incluem a emissão de um comando "pegar imagem" para uma câmera digital ainda.

Em WPD, esses comportamentos são descritos pela representação do dispositivo como uma hierarquia de objetos. A ilustração a seguir mostra uma representação de objeto WPD para um dispositivo de várias funções, que nesse caso é um telefone celular.

![ilustração mostrando a hierarquia de objetos para um telefone celular](images/wpd-overview-figure3.gif)

Essa hierarquia ilustra a funcionalidade e o conteúdo a seguir.

Função

-   Objeto de armazenamento. Este dispositivo tem armazenamento de dados.
-   Serviço de contatos. Esse serviço é um objeto funcional que pode ser usado para sincronizar e armazenar contatos no telefone.
-   Serviço SMS. Esse serviço é um objeto funcional que pode ser usado para enviar, receber e armazenar mensagens SMS.

Conteúdo:

-   Objetos de mídia. Este dispositivo armazena imagens, música e arquivos de vídeo em pastas no objeto de armazenamento. Embora os arquivos mostrados na ilustração sejam armazenados em uma pasta, um dispositivo pode subdividir o conteúdo em pastas organizadas pelo tipo de mídia armazenada; por exemplo, pastas de imagens, pastas de música e pastas de vídeo.
-   Objetos de contato. Este dispositivo armazena informações de contato (como nome, número de telefone e endereço) como filhos do serviço de contatos
-   Objetos de mensagem. Esse dispositivo armazena mensagens SMS como filhos do serviço SMS.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do aplicativo**](application-overview.md)
</dt> </dl>

 

 



