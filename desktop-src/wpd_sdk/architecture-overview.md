---
description: Visão geral da arquitetura
ms.assetid: ff20d83a-e9cd-46e9-95f7-3ebdf791e667
title: Visão geral da arquitetura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f911a14e60465efc8f8f8d798b7ddf527bf4e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837015"
---
# <a name="architecture-overview"></a>Visão geral da arquitetura

A arquitetura WPD pode ser dividida em três processos. Dentro desses processos estão os três principais componentes de WPD: a API, o serializador e o driver. A ilustração a seguir descreve os processos e componentes que constituem a arquitetura WPD.

![ilustração mostrando componentes de API, serializador e driver de WPD](images/wpd-overview-figure1.gif)

## <a name="the-wpd-application-programming-interface"></a>A interface de programação de aplicativos WPD

A API WPD é implementada como um servidor COM em processamento. A API usa APIs padrão do Microsoft Win32 para se comunicar com o driver WPD apropriado. Um componente chamado de serializador WPD é usado por ambos os objetos de API e pelo driver para empacotar ou desempacotar parâmetros para ou do Windows Driver Foundation (WDF)-buffers do UMDF (estrutura de driver de modo de usuário).

## <a name="the-wpd-serializer"></a>O serializador WPD

O serializador WPD é implementado como um servidor COM em processamento. A API WPD usa o serializador para empacotar comandos e parâmetros em buffers de mensagens que são enviados para o driver. O driver usa o serializador para desempacotar esses buffers de mensagens para processamento. O driver também usa o serializador para empacotar dados e parâmetros em buffers de resposta que são retornados para a API WPD, e a API WPD usa o serializador para desempacotar esses buffers de resposta para retornar aos chamadores.

## <a name="wpd-driver"></a>Driver WPD

O driver WPD é implementado como um driver padrão de estrutura de driver de modo de usuário (WDF) do Windows Driver Foundation (UMDF). Os drivers WPD são hospedados pelo UMDF em um processo separado chamado host do driver.

O driver recebe mensagens do refletor UMDF (isso não é mostrado no diagrama, já que o modo como os buffers são recebidos não é importante para o driver. Consulte a documentação do UMDF para obter mais informações). O Driver implementa um manipulador IOCL (código de controle de e/s específico de WPD) para processar as mensagens WPD recebidas pela API WPD. O driver usa o serializador WPD para desempacotar comandos e parâmetros desses buffers de mensagens e para empacotar a resposta no buffer de retorno.

Os drivers WPD podem se comunicar com seus dispositivos passando por um driver de modo kernel, normalmente acessado por meio de operações de arquivo Win32 (ou seja, CreateFile, ReadFile, WriteFile e assim por diante). Para os barramentos comuns, a Microsoft fornecerá drivers de kernel padrão para os fornecedores usarem, o que permitirá que os fornecedores enviem uma solução de driver somente de modo de usuário. Além disso, para os dispositivos MTP (protocolo de transferência de mídia) e MSC (classe de armazenamento em massa), a Microsoft fornecerá drivers de classe WPD.

Para obter mais informações sobre drivers WPD, consulte a documentação do driver de dispositivos portáteis do Windows no kit de driver do Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do aplicativo**](application-overview.md)
</dt> </dl>

 

 



