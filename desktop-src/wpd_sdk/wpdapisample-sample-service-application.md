---
description: Aplicativo WpdServicesApiSample
ms.assetid: 857753f7-bca1-4f4a-a8f9-0b2232e2f0dc
title: Aplicativo WpdServicesApiSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54cbf6c6e4647744ae45f43b5d4139cbf7f9dc55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755493"
---
# <a name="wpdservicesapisample-application"></a>Aplicativo WpdServicesApiSample

Um serviço de dispositivo é uma extensão de um objeto funcional: além de agrupar logicamente os recursos do dispositivo, um serviço de dispositivo fornece aos aplicativos a capacidade de descobrir programaticamente esses recursos.

O aplicativo de exemplo WpdServicesApiSample é um aplicativo de área de trabalho de linha de comando que você pode usar para explorar os serviços de contatos em dispositivos conectados ao seu computador. Você pode explorar esses serviços por meio da listagem com suporte: formatos, eventos, métodos e serviços abstratos. Você também pode usar esse aplicativo para recuperar as propriedades em um determinado serviço de contato e para invocar métodos com suporte nesse serviço.

Se você ainda não tiver um dispositivo que dê suporte a serviços de contatos, ainda poderá executar o WpdServicesApiSample se instalar primeiro o WpdServiceSampleDriver que está incluído no kit de driver do Windows.

O aplicativo de exemplo WpdServicesApiSample inclui os seguintes arquivos:



| **Arquivo**                | **Descrição**                                                                                                                                                                                           |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ContentEnumeration. cpp  | Contém métodos que enumeram o conteúdo em um determinado serviço Contacts.                                                                                                                                  |
| Contentproperties. cpp   | Contém métodos que lêem e gravam Propriedades em um determinado serviço de contatos.                                                                                                                              |
| Percapabilities. cpp | Contém os métodos que recuperam os formatos com suporte, os eventos e os serviços abstratos que são suportados por um determinado serviço de contatos.                                                                   |
| O inenumeration. cpp  | Contém as funções auxiliares que recuperam informações do dispositivo, como o nome amigável do dispositivo ou os serviços de contatos com suporte.                                                                       |
| Permethods. cpp      | Contém os métodos que recuperam e invocam métodos com suporte de um determinado serviço de contatos.                                                                                                              |
| Stdafx.cpp              | Inclui os arquivos padrão.                                                                                                                                                                              |
| WpdServiceApiSample. cpp | Hospeda a função de inicialização **\_ tmain** , que chama a função **domenu** local, que exibe uma lista de dispositivos e tarefas disponíveis e chama a função apropriada para a seleção de menu do usuário. |



 


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Amostras](sample.md)
</dt> </dl>

 

 



