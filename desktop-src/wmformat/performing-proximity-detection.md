---
title: Executando detecção de proximidade
description: Executando detecção de proximidade
ms.assetid: 73207c4c-2d8d-4ec3-b3d0-78f55ee0a754
keywords:
- SDK do Windows Media Format, executando detecção de proximidade
- SDK do Windows Media Format, detecção de proximidade
- ASF (Advanced Systems Format), executando detecção de proximidade
- ASF (formato de sistemas avançados), executando detecção de proximidade
- ASF (Advanced Systems Format), detecção de proximidade
- ASF (formato de sistemas avançados), detecção de proximidade
- DRM (gerenciamento de direitos digitais), executando detecção de proximidade
- DRM (gerenciamento de direitos digitais), executando detecção de proximidade
- DRM (gerenciamento de direitos digitais), detecção de proximidade
- DRM (gerenciamento de direitos digitais), detecção de proximidade
- detecção de proximidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9628a6c33832b56858e5c457f15fd0935c2c436
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365523"
---
# <a name="performing-proximity-detection"></a>Executando detecção de proximidade

Antes de poder transmitir dados criptografados para um dispositivo registrado no protocolo Windows Media DRM 10 para dispositivos de rede, você deve executar um processo chamado detecção de proximidade (também chamado de validação). Esse processo envolve o envio de mensagens para o dispositivo e o recebimento de respostas. O tempo necessário para receber uma resposta é usado para determinar se o dispositivo é "próximo" o suficiente para o computador na rede para receber dados seguros. A confirmação de que o dispositivo está fisicamente perto do computador cliente na rede ajuda a impedir falsificação e outro acesso não autorizado.

Quando a detecção de proximidade for concluída com êxito, o dispositivo será considerado válido. Você pode verificar se um dispositivo é válido chamando o método [**IWMRegisteredDevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) . Os dispositivos devem ser validados a cada 48 horas. Um dispositivo que foi validado mais de 48 horas antes da execução do programa deve ser revalidado executando o processo de detecção de proximidade novamente.

Para executar a detecção de proximidade, você deve estabelecer comunicações com o dispositivo e, em seguida, chamar o método [**IWMProximityDetection:: StartDetection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) . O processo de detecção é concluído de forma assíncrona pelos componentes DRM internos do SDK do Windows Media Format. Seu aplicativo deve incluir uma implementação da interface [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) para processar mensagens de detecção de proximidade.

Há duas mensagens enviadas pelo processo de detecção de proximidade: uma mensagem de resultado e uma mensagem de conclusão.

A mensagem de resultado, \_ resultado de proximidade WMT \_ , é enviada quando o processo de detecção é concluído. O parâmetro *HR* do método de retorno de chamada [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) indica se o dispositivo foi considerado quase o suficiente para o computador cliente. Se o parâmetro *HR* da mensagem de resultado indicar êxito *, o parâmetro* 1h conterá um **DWORD** especificando a latência medida para o dispositivo em milissegundos.

A mensagem de conclusão, \_ proximidade de WMT \_ concluída, é enviada quando a detecção é finalizada. Você deve liberar a interface [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) somente depois de receber essa mensagem.

Quando a detecção de proximidade de um dispositivo é realizada com sucesso, o banco de dados de registro de dispositivo é atualizado automaticamente. As chamadas subsequentes para [**IWMRegisteredDevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) retornará **TRUE** até que 48 horas tenham passado e o dispositivo precise ser revalidado.

**Observação** O DRM não é compatível com a versão baseada em x64 deste SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando o protocolo Windows Media DRM 10 para dispositivos de rede**](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




