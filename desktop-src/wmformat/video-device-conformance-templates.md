---
title: Modelos de conformidade do dispositivo de vídeo
description: Modelos de conformidade do dispositivo de vídeo
ms.assetid: 0a91167c-8799-4ce8-a377-c4e613567d0f
keywords:
- Windows SDK de Formato de Mídia, modelos de conformidade do dispositivo
- ASF (Advanced Systems Format), modelos de conformidade do dispositivo
- ASF (Formato de Sistemas Avançados), modelos de conformidade do dispositivo
- Windows SDK de Formato de Mídia, modelos de conformidade do dispositivo de vídeo
- ASF (Advanced Systems Format), modelos de conformidade do dispositivo de vídeo
- ASF (Formato de Sistemas Avançados), modelos de conformidade do dispositivo de vídeo
- Windows Codec do Vídeo de Mídia 9, modelos de conformidade do dispositivo de vídeo
- codecs,Windows Media Video 9 codec
- modelos de conformidade do dispositivo, vídeo
- modelos de conformidade do dispositivo de vídeo
- modelos, modelos de conformidade do dispositivo de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df63d40152e814f879498f0f99e386c9b21ef1e32746cf0c405aa46ab9d2fa48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584836"
---
# <a name="video-device-conformance-templates"></a>Modelos de conformidade do dispositivo de vídeo

As tabelas a seguir listam os modelos de conformidade do dispositivo e os parâmetros associados para o codec Windows Media Video 9.

## <a name="simple-profile-low-level"></a>Perfil Simples, Nível Baixo



| Parâmetro                                | Valor                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------|
| Cadeia de caracteres de modelo                          | "SP@LL"                                                                               |
| Dispositivos apropriados                      | Dispositivos sem fio (Microsoft Windows-Powered SmartPhone e dispositivos semelhantes) |
| Resolução máxima                       | 176 x 144                                                                             |
| Taxa máxima de quadros                       | 15 fps                                                                                |
| Taxa de bits máxima                         | 96 Kbps                                                                               |
| Tamanho máximo do buffer (em unidades de 16384 bits) | 20 (cerca de 3,4 segundos na taxa máxima de bits)                                            |
| Codificação entrelaçada                      | Não                                                                                    |



 

## <a name="simple-profile-medium-level"></a>Perfil Simples, Nível Médio



| Parâmetro                                | Valor                                                                                |
|------------------------------------------|--------------------------------------------------------------------------------------|
| Cadeia de caracteres de modelo                          | "SP@ML"                                                                              |
| Dispositivos apropriados                      | Computadores portáteis e assistentes de dados pessoaisSem seus dispositivos sem fio de ponta<br/> |
| Resolução máxima                       | 352 x 288                                                                            |
| Taxa máxima de quadros                       | 15 fps @ 352 x 28824 fps @ 320 x 240<br/>                                      |
| Taxa de bits máxima                         | 384 Kbps                                                                             |
| Tamanho máximo do buffer (em unidades de 16384 bits) | 77 (cerca de 3,3 segundos na taxa máxima de bits)                                           |
| Codificação entrelaçada                      | Não                                                                                   |



 

## <a name="generic-simple-profile"></a>Perfil Simples Genérico

Um fluxo que está em conformidade com as limitações algorítmicas do perfil simples, mas não se ajusta a uma das especificações de nível, será atribuído "SP" como sua cadeia de caracteres de modelo de conformidade do dispositivo.

## <a name="main-profile-low-level"></a>Perfil Principal, Nível Baixo



| Parâmetro                                | Valor                                       |
|------------------------------------------|---------------------------------------------|
| Cadeia de caracteres de modelo                          | "MP@LL"                                     |
| Dispositivos apropriados                      | Caixas set-top                               |
| Resolução máxima                       | 352 x 288                                   |
| Taxa máxima de quadros                       | 30 fps                                      |
| Taxa de bits máxima                         | 2 Mbps                                      |
| Tamanho máximo do buffer (em unidades de 16384 bits) | 306 (cerca de 2,5 segundos na taxa máxima de bits) |
| Codificação entrelaçada                      | Não                                          |



 

## <a name="main-profile-medium-level"></a>Perfil Principal, Nível Médio



| Parâmetro                                | Valor                                                                                                                  |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Cadeia de caracteres de modelo                          | "MP@ML"                                                                                                                |
| Dispositivos apropriados                      | Caixas set-topSlower computers using DirectX Video Acceleration<br/> Windows Players de DVD habilitados para mídia<br/> |
| Resolução máxima                       | 720 x 576                                                                                                              |
| Taxa máxima de quadros                       | 30 fps @ 720 x 48025 fps @ 720 x 576<br/>                                                                        |
| Taxa de bits máxima                         | 10 Mbps                                                                                                                |
| Tamanho máximo do buffer (em unidades de 16384 bits) | 611 (cerca de 1 segundo na taxa máxima de bits)                                                                               |
| Codificação entrelaçada                      | Sim                                                                                                                    |



 

## <a name="main-profile-high-level"></a>Perfil Principal, Alto Nível



| Parâmetro                                | Valor                                                                                                                                                                 |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cadeia de caracteres de modelo                          | "MP@HL"                                                                                                                                                               |
| Dispositivos apropriados                      | Computadores que usam players de DVD habilitados para AccelerationHigh-Definition Windows mídia do DirectX<br/> Ambiente digital<br/> streaming de alta definição<br/> |
| Resolução máxima                       | 1920 x 1080                                                                                                                                                           |
| Taxa máxima de quadros                       | 30 fps @ 1920 x 108060 fps @ 1280 x 720<br/>                                                                                                                    |
| Taxa de bits máxima                         | 20 Mbps                                                                                                                                                               |
| Tamanho máximo do buffer (em unidades de 16384 bits) | 2442 (cerca de 2,66 segundos na taxa máxima de bits)                                                                                                                         |
| Codificação entrelaçada                      | Sim                                                                                                                                                                   |



 

## <a name="generic-main-profile"></a>Perfil Principal Genérico

Um fluxo que está em conformidade com as limitações algorítmicas do perfil principal, mas não se ajusta a uma das especificações de nível, será atribuído "MP" como sua cadeia de caracteres de modelo de conformidade do dispositivo.

## <a name="complex-profile"></a>Perfil Complexo



| Parâmetro       | Valor                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Cadeia de caracteres de modelo | "CP"                                                                                                                                   |
| Comentários         | O perfil complexo não tem limitações explícitas. Ele é usado para habilitar todos os algoritmos de codec, geralmente para fins de demonstração. |



 

As tabelas a seguir listam os parâmetros dos modelos de conformidade do dispositivo para o codec Windows Imagem do Vídeo de Mídia 9.

## <a name="video-image-level-1"></a>Nível de imagem de vídeo 1



| Parâmetro                                | Valor                                       |
|------------------------------------------|---------------------------------------------|
| Cadeia de caracteres de modelo                          | "I1"                                        |
| Resolução máxima                       | 352 x 288                                   |
| Taxa máxima de quadros                       | 30 fps                                      |
| Taxa de bits máxima                         | 192Kbps                                    |
| Tamanho máximo do buffer (em unidades de 16384 bits) | 39 (cerca de 3,26 segundos na taxa máxima de bits) |
| Codificação entrelaçada                      | Não                                          |



 

## <a name="video-image-level-2"></a>Nível de imagem de vídeo 2



| Parâmetro                                | Valor                                       |
|------------------------------------------|---------------------------------------------|
| Cadeia de caracteres de modelo                          | "I2"                                        |
| Resolução máxima                       | 1024 x 768                                  |
| Taxa máxima de quadros                       | 30 fps                                      |
| Taxa de bits máxima                         | 384 Kbps                                    |
| Tamanho máximo do buffer (em unidades de 16384 bits) | 77 (cerca de 3,26 segundos na taxa máxima de bits) |
| Codificação entrelaçada                      | Não                                          |



 

## <a name="generic-video-image"></a>Imagem de vídeo genérica

Um fluxo de Imagem de Vídeo que não se ajusta a uma das especificações de nível receberá "I" como sua cadeia de caracteres de modelo de conformidade do dispositivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Modelos de conformidade do dispositivo de áudio**](audio-device-conformance-templates.md)
</dt> <dt>

[**Parâmetros do modelo de conformidade do dispositivo**](device-conformance-template-parameters.md)
</dt> <dt>

[**Combinações de modelo de conformidade de dispositivo recomendadas**](recommended-device-conformance-template-combinations.md)
</dt> </dl>

 

 





