---
description: Um cliente XAudio2 tem controle total do mapeamento dos canais de uma voz para os canais de cada uma de suas vozes de destino.
ms.assetid: 219d5b70-3f07-f973-f9ec-1cb3cf0be37e
title: XAudio2 mapeamento de canal padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06d77371223ccef02d6f0831a7aea182326f8477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461344"
---
# <a name="xaudio2-default-channel-mapping"></a>XAudio2 mapeamento de canal padrão

Um cliente XAudio2 tem controle total do mapeamento dos canais de uma voz para os canais de cada um de seus voicesIt de destino controla o mapeamento por meio do uso do método [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) . Em algumas circunstâncias, no entanto, o XAudio2 simplifica essa tarefa Configurando automaticamente uma matriz de envio padrão. Ele faz isso usando a máscara de canal, se houver, associada aos canais de áudio de uma voz. Uma máscara de canal é uma combinação de \_ máscaras de bits do orador xxx, conforme definido em X3DAudio. h e em outro lugar. XAudio2 exige que as máscaras de canal sejam 0 ou tenham o mesmo número de bits definido como o número de canais.

A tabela a seguir mostra os requisitos de máscara de canal e padrões para os formatos com suporte pelo XAudio2. 

| Formatar | Requisito de máscara de canal             | Máscara padrão                        | Membro da estrutura correspondente                            |
|--------|--------------------------------------|-------------------------------------|-----------------------------------------------------------|
| PCM    | O arquivo pode conter uma máscara de canal    | A máscara de canal é 0 ou ausente        | WAVEFORMATEXTENSIBLE. dwChannelMask ou None (WAVEFORMATEX) |
| ADPCM  | O arquivo não contém uma máscara de canal | A máscara de canal padrão sempre é usada | Nenhum (ADPCMWAVEFORMAT)                                    |



 

Para as vozes submix e de mestre, e para as vozes de origem sem uma máscara de canal ou uma máscara de canal de 0, XAudio2 assume as posições de alto-falantes padrão de acordo com a tabela a seguir. 

| Canais  | Posições de canal implícitas                                                                                            |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| 1         | Sempre mapeia para FrontLeft e FrontRight em escala total em ambos os alto-falantes (caso especial para sons mono)                 |
| 2         | FrontLeft, FrontRight (configuração básica de estéreo)                                                                    |
| 3         | FrontLeft, FrontRight, LowFrequency (configuração de 2,1)                                                               |
| 4         | FrontLeft, FrontRight, esquerda, direita (Quadraphonic)                                                             |
| 5         | FrontLeft, FrontRight, FrontCenter, SideLeft, SideRight (configuração de 5,0)                                           |
| 6         | FrontLeft, FrontRight, FrontCenter, LowFrequency, SideLeft, SideRight (configuração de 5,1) (consulte os seguintes comentários) |
| 7         | FrontLeft, FrontRight, FrontCenter, LowFrequency, SideLeft, SideRight, backcenter (configuração de 6,1)                 |
| 8         | FrontLeft, FrontRight, FrontCenter, LowFrequency, esquerda, direita, SideLeft, SideRight (configuração de 7,1)        |
| 9 ou mais | Sem posições implícitas (mapeamento um-para-um)                                                                            |



 

Se um par de voz específico no grafo de áudio não tiver nenhuma posição de orador associada à sua voz de origem ou de destino (uma voz tem mais de oito canais), nenhuma voz será reproduzida até que a voz de origem tenha uma matriz de envio definida explicitamente usando o método [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) . Chamar o método [**IXAudio2SourceVoice:: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) para qualquer voz falhará até que você faça isso.

Se a voz de origem e a voz de destino tiverem números diferentes de posições de alto-falante e [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) não for chamado na voz de origem, XAudio2 enviará cada canal de origem para o alto-falante de destino mais próximo (ou os alto-falantes), proporcionalmente ao quão perto eles são para o orador pretendido. Há dois casos especiais em que o comportamento padrão é diferente.

1.  Se o áudio de origem for mono e estiver posicionado no front Center do alto-falante \_ \_ ou não tiver nenhuma posição definida, ele será sempre enviado para o lado frontal do alto-falante \_ \_ e a \_ frente do orador \_ se existirem no áudio de saída. Se eles não existirem, ele retornará ao caso normal.
2.  Se a origem e o destino forem de 6 canais e estiverem posicionados em qualquer uma das configurações de alto-falante padrão de 5,1 (esquerda + direita + centro + parte + de trás + verso ou esquerda + direita + centro + sub+ Laterall + SideR), os canais serão mapeados por meio de um para um. Em outras palavras, SideLeft/Right e esquerdo/direito são tratados de maneira equivalente. Isso ocorre porque houve confusão histórica em relação a essas configurações. Portanto, a intenção assumida é sempre mapear uma para uma.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vozes](voices.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> <dt>

[**GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask)
</dt> </dl>

 

 
