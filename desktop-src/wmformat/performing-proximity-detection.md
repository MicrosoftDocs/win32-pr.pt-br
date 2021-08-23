---
title: Executando a detecção de proximidade
description: Executando a detecção de proximidade
ms.assetid: 73207c4c-2d8d-4ec3-b3d0-78f55ee0a754
keywords:
- Windows SDK de Formato de Mídia, executando a detecção de proximidade
- Windows SDK de Formato de Mídia, detecção de proximidade
- ASF (Advanced Systems Format), executando a detecção de proximidade
- ASF (Formato de Sistemas Avançados), executando a detecção de proximidade
- ASF (Advanced Systems Format), detecção de proximidade
- ASF (Formato de Sistemas Avançados), detecção de proximidade
- DRM (gerenciamento de direitos digitais), executando a detecção de proximidade
- DRM (gerenciamento de direitos digitais), executando a detecção de proximidade
- DRM (gerenciamento de direitos digitais), detecção de proximidade
- DRM (gerenciamento de direitos digitais), detecção de proximidade
- detecção de proximidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181b13d56e4c2b1fea0da1ff761f6d915680ff89c42747b9faf4260184ae4205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963975"
---
# <a name="performing-proximity-detection"></a>Executando a detecção de proximidade

Antes de transmitir dados criptografados para um dispositivo registrado no protocolo WINDOWS Media DRM 10 para Dispositivos de Rede, você deve executar um processo chamado detecção de proximidade (também chamado de validação). Esse processo envolve o envio de mensagens para o dispositivo e o recebimento de respostas. O tempo necessário para receber uma resposta é usado para determinar se o dispositivo está "próximo" o suficiente para o computador na rede receber dados seguros. Confirmar que o dispositivo está fisicamente próximo ao computador cliente na rede ajuda a evitar a fraude e outros acessos não autorizados.

Quando a detecção de proximidade é concluída com êxito, diz-se que o dispositivo é válido. Você pode verificar se um dispositivo é válido chamando o [**método IWMRegisteredDevice::IsValid.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) Os dispositivos devem ser validados a cada 48 horas. Um dispositivo que foi validado mais de 48 horas antes da execução do programa deve ser revalidado executando o processo de detecção de proximidade novamente.

Para executar a detecção de proximidade, você deve estabelecer comunicações com o dispositivo e, em seguida, chamar o método [**IWMProximityDetection::StartDetection.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) O processo de detecção é concluído de forma assíncrona pelos componentes internos do DRM do SDK Windows Formato de Mídia. Seu aplicativo deve incluir uma implementação da interface [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) para processar mensagens de detecção de proximidade.

Há duas mensagens enviadas pelo processo de detecção de proximidade: uma mensagem de resultado e uma mensagem de conclusão.

A mensagem de resultado, WMT \_ PROXIMITY \_ RESULT, é enviada quando o processo de detecção é concluído. O *parâmetro hr* do método de retorno de chamada [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) indica se o dispositivo foi encontrado próximo o suficiente para o computador cliente. Se o *parâmetro hr* da mensagem de resultado indicar êxito, o parâmetro *pValue* conterá um **DWORD** especificando a latência medida para o dispositivo em milissegundos.

A mensagem de conclusão, WMT \_ PROXIMITY \_ COMPLETED, é enviada quando a detecção é finalizada. Você deve liberar a interface [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) somente depois de receber essa mensagem.

Quando a detecção de proximidade de um dispositivo é bem-sucedida, o banco de dados de registro do dispositivo é atualizado automaticamente. Chamadas subsequentes [**para IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) retornarão **TRUE** até que 48 horas tenham passado e o dispositivo precise ser revalidado.

**Observação** O DRM não é suportado pela versão baseada em x64 deste SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando o Windows DRM de mídia 10 para o protocolo de dispositivos de rede**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




