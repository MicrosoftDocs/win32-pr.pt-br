---
description: Visão geral da arquitetura
ms.assetid: ff20d83a-e9cd-46e9-95f7-3ebdf791e667
title: Visão geral da arquitetura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76eafce326655a4d9386d37c02df9ef0ab2b9772b5e87eedaff40a19383b2cec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590457"
---
# <a name="architecture-overview"></a>Visão geral da arquitetura

A arquitetura WPD pode ser dividida em três processos. Dentro desses processos estão os três componentes principais do WPD: a API, o serializador e o driver. A ilustração a seguir ilustra os processos e componentes que constituem a arquitetura WPD.

![ilustração mostrando componentes de API, serializador e driver do wpd](images/wpd-overview-figure1.gif)

## <a name="the-wpd-application-programming-interface"></a>A interface de programação de aplicativo WPD

A API WPD é implementada como um servidor COM em processo. A API usa APIs padrão do Microsoft Win32 para se comunicar com o driver WPD apropriado. Um componente chamado serializador WPD é usado por objetos de API e pelo driver para empacotar ou desempacotar parâmetros de ou para buffers do WDF (Windows Driver Foundation)-USER-User-Mode Driver Framework (UMDF).

## <a name="the-wpd-serializer"></a>O serializador WPD

O serializador WPD é implementado como um servidor COM em processo. A API WPD usa o serializador para empacotar comandos e parâmetros em buffers de mensagem que são enviados ao driver. O driver usa o serializador para desempacotar esses buffers de mensagem para processamento. O driver também usa o serializador para empacotar dados e parâmetros em buffers de resposta retornados para a API WPD e a API WPD usa o serializador para desempacotar esses buffers de resposta para retornar aos chamadores.

## <a name="wpd-driver"></a>WPD Driver

O driver WPD é implementado como um driver padrão do WDF (Driver Foundation do Windows)-USER-User-Mode Driver Framework (UMDF). Os drivers WPD são hospedados pelo UMDF em um processo separado chamado Host do Driver.

O driver recebe mensagens do refletor UMDF (isso não é mostrado no diagrama, pois como os buffers são recebidos não é importante para o driver. Confira a documentação do UMDF para obter mais informações). O driver implementa um manipulador de IOCL (código de controle de E/S) específico de WPD para processar mensagens WPD recebidas pela API WPD. O driver usa o serializador WPD para desempacotar comandos e parâmetros desses buffers de mensagem e empacotar a resposta no buffer de retorno.

Os drivers WPD podem se comunicar com seus dispositivos passando por um driver de modo kernel, normalmente acessado por meio de operações de arquivo Win32 (ou seja, CreateFile, ReadFile, WriteFile e assim por diante). Para os caminhões comuns, a Microsoft fornecerá drivers de kernel padrão para os fornecedores usarem, o que permitirá que os fornecedores forneçam uma solução de driver somente no modo de usuário. Além disso, para dispositivos MTP (Media Transfer Protocol) e MSC (Mass Armazenamento Class), a Microsoft fornecerá drivers de classe WPD.

Para obter mais informações sobre drivers WPD, consulte a documentação Windows driver de dispositivos portáteis no kit de Windows driver.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do aplicativo**](application-overview.md)
</dt> </dl>

 

 



