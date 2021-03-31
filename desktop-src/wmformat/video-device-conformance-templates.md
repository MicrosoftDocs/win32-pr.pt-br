---
title: Modelos de conformidade de dispositivo de vídeo
description: Modelos de conformidade de dispositivo de vídeo
ms.assetid: 0a91167c-8799-4ce8-a377-c4e613567d0f
keywords:
- SDK do Windows Media Format, modelos de conformidade do dispositivo
- ASF (Advanced Systems Format), modelos de conformidade do dispositivo
- ASF (formato de sistemas avançados), modelos de conformidade do dispositivo
- SDK do Windows Media Format, modelos de conformidade de dispositivo de vídeo
- ASF (Advanced Systems Format), modelos de conformidade de dispositivo de vídeo
- ASF (formato de sistemas avançados), modelos de conformidade de dispositivo de vídeo
- Codec do Windows Media Video 9, modelos de conformidade de dispositivo de vídeo
- codecs, codec do Windows Media Video 9
- modelos de conformidade do dispositivo, vídeo
- modelos de conformidade de dispositivo de vídeo
- modelos, modelos de conformidade de dispositivo de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc6735d029bc2339296fa2a0af8a48ace3303ae3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823020"
---
# <a name="video-device-conformance-templates"></a>Modelos de conformidade de dispositivo de vídeo

As tabelas a seguir listam os modelos de conformidade do dispositivo e os parâmetros associados para o codec do Windows Media Video 9.

## <a name="simple-profile-low-level"></a>Perfil simples, nível baixo



| Parâmetro                                | Valor                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------|
| Cadeia de caracteres do modelo                          | "SP@LL"                                                                               |
| Dispositivos apropriados                      | Telefones sem fio (solução Microsoft Windows-Powered SmartPhone e dispositivos semelhantes) |
| Resolução máxima                       | 176 x 144                                                                             |
| Taxa máxima de quadros                       | 15 fps                                                                                |
| Taxa de bits máxima                         | 96 kbps                                                                               |
| Tamanho máximo do buffer (em unidades de 16384 bits) | 20 (cerca de 3,4 segundos a taxa de bits máxima)                                            |
| Codificação entrelaçada                      | Não                                                                                    |



 

## <a name="simple-profile-medium-level"></a>Perfil simples, nível médio



| Parâmetro                                | Valor                                                                                |
|------------------------------------------|--------------------------------------------------------------------------------------|
| Cadeia de caracteres do modelo                          | "SP@ML"                                                                              |
| Dispositivos apropriados                      | Computadores de mão e aparelhos de telefone assistantsHigh de dados pessoais de ponta<br/> |
| Resolução máxima                       | 352 x 288                                                                            |
| Taxa máxima de quadros                       | 15 fps @ 352 x 28824 de FPS @ 320 x 240<br/>                                      |
| Taxa de bits máxima                         | 384 kbps                                                                             |
| Tamanho máximo do buffer (em unidades de 16384 bits) | 77 (cerca de 3,3 segundos a taxa máxima de bits)                                           |
| Codificação entrelaçada                      | Não                                                                                   |



 

## <a name="generic-simple-profile"></a>Perfil simples genérico

Um fluxo que está em conformidade com as limitações de algoritmos do perfil simples, mas que não se encaixa em uma das especificações de nível, será atribuído "SP" como sua cadeia de caracteres de modelo de conformidade do dispositivo.

## <a name="main-profile-low-level"></a>Perfil principal, nível baixo



| Parâmetro                                | Valor                                       |
|------------------------------------------|---------------------------------------------|
| Cadeia de caracteres do modelo                          | "MP@LL"                                     |
| Dispositivos apropriados                      | Conjunto-caixas superiores                               |
| Resolução máxima                       | 352 x 288                                   |
| Taxa máxima de quadros                       | 30 fps                                      |
| Taxa de bits máxima                         | 2 Mbps                                      |
| Tamanho máximo do buffer (em unidades de 16384 bits) | 306 (cerca de 2,5 segundos a taxa máxima de bits) |
| Codificação entrelaçada                      | Não                                          |



 

## <a name="main-profile-medium-level"></a>Perfil principal, nível médio



| Parâmetro                                | Valor                                                                                                                  |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Cadeia de caracteres do modelo                          | "MP@ML"                                                                                                                |
| Dispositivos apropriados                      | Set-principais computadores boxesSlower usando a aceleração de vídeo do DirectX<br/> Players de DVD habilitados para Windows Media<br/> |
| Resolução máxima                       | 720 x 576                                                                                                              |
| Taxa máxima de quadros                       | 30 fps @ 720 x 48025 de FPS @ 720 x 576<br/>                                                                        |
| Taxa de bits máxima                         | 10 Mbps                                                                                                                |
| Tamanho máximo do buffer (em unidades de 16384 bits) | 611 (cerca de 1 segundo na taxa de bits máxima)                                                                               |
| Codificação entrelaçada                      | Sim                                                                                                                    |



 

## <a name="main-profile-high-level"></a>Perfil principal, alto nível



| Parâmetro                                | Valor                                                                                                                                                                 |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cadeia de caracteres do modelo                          | "MP@HL"                                                                                                                                                               |
| Dispositivos apropriados                      | Computadores usando vídeo DirectX AccelerationHigh-Definition players de DVD habilitados para Windows Media<br/> Cinema digital<br/> streaming de alta definição<br/> |
| Resolução máxima                       | 1920 x 1080                                                                                                                                                           |
| Taxa máxima de quadros                       | 30 fps @ 1920 x 108060 de FPS @ 1280 x 720<br/>                                                                                                                    |
| Taxa de bits máxima                         | 20 Mbps                                                                                                                                                               |
| Tamanho máximo do buffer (em unidades de 16384 bits) | 2442 (cerca de 2,66 segundos a taxa máxima de bits)                                                                                                                         |
| Codificação entrelaçada                      | Sim                                                                                                                                                                   |



 

## <a name="generic-main-profile"></a>Perfil principal genérico

Um fluxo que está em conformidade com as limitações de algoritmos do perfil principal, mas que não se encaixa em uma das especificações de nível, será atribuído "MP" como sua cadeia de caracteres de modelo de conformidade do dispositivo.

## <a name="complex-profile"></a>Perfil complexo



| Parâmetro       | Valor                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Cadeia de caracteres do modelo | CP                                                                                                                                   |
| Comentários         | O perfil complexo não tem limitações explícitas. Ele é usado para habilitar todos os algoritmos de codec, geralmente para fins de demonstração. |



 

As tabelas a seguir listam os parâmetros dos modelos de conformidade do dispositivo para o codec de imagem do Windows Media Video 9.

## <a name="video-image-level-1"></a>Nível de imagem de vídeo 1



| Parâmetro                                | Valor                                       |
|------------------------------------------|---------------------------------------------|
| Cadeia de caracteres do modelo                          | I1                                        |
| Resolução máxima                       | 352 x 288                                   |
| Taxa máxima de quadros                       | 30 fps                                      |
| Taxa de bits máxima                         | 192Kbps                                    |
| Tamanho máximo do buffer (em unidades de 16384 bits) | 39 (cerca de 3,26 segundos a taxa máxima de bits) |
| Codificação entrelaçada                      | Não                                          |



 

## <a name="video-image-level-2"></a>Nível de imagem de vídeo 2



| Parâmetro                                | Valor                                       |
|------------------------------------------|---------------------------------------------|
| Cadeia de caracteres do modelo                          | I2                                        |
| Resolução máxima                       | 1024 x 768                                  |
| Taxa máxima de quadros                       | 30 fps                                      |
| Taxa de bits máxima                         | 384 kbps                                    |
| Tamanho máximo do buffer (em unidades de 16384 bits) | 77 (cerca de 3,26 segundos a taxa máxima de bits) |
| Codificação entrelaçada                      | Não                                          |



 

## <a name="generic-video-image"></a>Imagem de vídeo genérica

Um fluxo de imagem de vídeo que não caiba em uma das especificações de nível será atribuído "I" como sua cadeia de caracteres de modelo de conformidade do dispositivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Modelos de conformidade do dispositivo de áudio**](audio-device-conformance-templates.md)
</dt> <dt>

[**Parâmetros do modelo de conformidade do dispositivo**](device-conformance-template-parameters.md)
</dt> <dt>

[**Combinações de modelo de conformidade do dispositivo recomendado**](recommended-device-conformance-template-combinations.md)
</dt> </dl>

 

 





