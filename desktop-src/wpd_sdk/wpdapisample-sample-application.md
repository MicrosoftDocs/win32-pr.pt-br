---
description: Aplicativo WpdApiSample
ms.assetid: 854a6304-5d62-4f00-9366-8c2244568250
title: Aplicativo WpdApiSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef1741f2cad07e28bee514cf6109cdbbf7347966e1a8184a88a11936cbccdcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963465"
---
# <a name="wpdapisample-application"></a>Aplicativo WpdApiSample

O aplicativo de exemplo WpdApiSample é um aplicativo de área de trabalho de linha de comando que permite enumerar dispositivos conectados, explorar dispositivos, consultar objetos para propriedades e atributos, enviar e recuperar objetos e assim por diante. Na inicialização, o aplicativo abre uma janela de comando que lista as tarefas que você pode executar.

O aplicativo de exemplo WpdApiSample inclui os seguintes arquivos:



| **Arquivo**               | **Descrição**                                                                                                                                                                                           |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ContentEnumeration. cpp | Contém funções que enumeram todos os objetos em um dispositivo.                                                                                                                                            |
| Contentproperties. cpp  | Contém funções que lêem e gravam Propriedades de objeto e fazem solicitações set/get de propriedade em massa.                                                                                                         |
| ContentTransfer. cpp    | Contém funções que transferem conteúdo de ou para o dispositivo, leem requisitos de tipo de objeto e criam uma pasta no dispositivo.                                                                         |
| DeviceCapabilities. cpp | Contém funções para listar os tipos de objeto funcional no dispositivo, listar os tipos de conteúdo com suporte em cada tipo de objeto funcional e exibir perfis de objeto de renderização.                             |
| DeviceEnumeration. cpp  | Lista os nomes amigáveis, fabricantes e descrições de todos os dispositivos conectados.                                                                                                                       |
| DeviceEvents. cpp       | Contém funções que registram eventos de dispositivo e seus parâmetros sempre que os eventos são acionados.                                                                                                                 |
| Stdafx.cpp             | Inclui os arquivos padrão.                                                                                                                                                                              |
| WpdApiSample. cpp       | Hospeda a função de inicialização **\_ tmain** , que chama a função **domenu** local, que exibe uma lista de dispositivos e tarefas disponíveis e chama a função apropriada para a seleção de menu do usuário. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Amostra](sample.md)
</dt> </dl>

 

 



