---
description: Atributos de topologia
ms.assetid: 50102096-a29f-4c00-a685-179ba5d71089
title: Atributos de topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db599a9d55e960bbb38043aa8932cd66ae0cbb6d9b376f403c1886faf3155c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972845"
---
# <a name="topology-attributes"></a>Atributos de topologia

Os atributos a seguir se aplicam a topologias.



| Atributo                                                                                                | Descrição                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MODO \_ \_ DXVA DE \_ TOPOLOGIA MF](mf-topology-dxva-mode.md)                                                    | Especifica se o carregador de topologia habilita a DXVA (Aceleração de Vídeo) do Microsoft DirectX na topologia.                                                                                                                         |
| [ALTERAÇÃO DINÂMICA \_ DE TOPOLOGIA \_ \_ MF \_ NÃO \_ PERMITIDA](mf-topology-dynamic-change-not-allowed.md)                | Especifica se a Sessão de Mídia tenta modificar a topologia quando o formato de um fluxo é modificado.                                                                                                                           |
| [TOPOLOGIA MF \_ \_ \_ HABILITAR XVP \_ PARA \_ REPRODUÇÃO](mf-topology-enable-xvp-for-playback.md)                | Especifica se o carregador de topologia habilita o XVP (Transcode Video Processor). para conversões, habilitando a conversão de cores acelerada por hardware.                                                                                        |
| [ENUMERAR TIPOS DE \_ \_ ORIGEM DA \_ \_ TOPOLOGIA MF](mf-topology-enumerate-source-types.md)                         | Especifica se o carregador de topologia enumera os tipos de mídia fornecidos pela fonte de mídia.                                                                                                                                     |
| [MODO DE \_ HARDWARE DE \_ \_ TOPOLOGIA MF](mf-topology-hardware-mode.md)                                            | Especifica se as transformação baseadas em hardware na topologia de de inclusão de .                                                                                                                                                            |
| [**TOPOLOGIA MF \_ \_ SEM \_ MARKIN \_ MARKOUT**](mf-topology-no-markin-markout-attribute.md)                     | Especifica se o pipeline corta amostras.                                                                                                                                                                                      |
| [TAXA DE QUADROS \_ DE REPRODUÇÃO DA TOPOLOGIA \_ \_ MF](mf-topology-playback-framerate.md)                                  | Especifica a taxa de atualização do monitor.                                                                                                                                                                                                |
| [DIMS MÁXIMO \_ DE REPRODUÇÃO DA TOPOLOGIA \_ \_ \_ MF](mf-topology-playback-max-dims.md)                                   | Especifica o tamanho da janela de destino para reprodução de vídeo.                                                                                                                                                                   |
| [**INÍCIO DO PROJETO \_ DE \_ TOPOLOGIA DO MF**](mf-topology-projectstart-attribute.md)                                 | Especifica a hora de início da topologia dentro do segmento atual, em unidades de 100 nanossegundos.                                                                                                                                             |
| [**PROJETOS DE \_ TOPOLOGIA DO MFTOP \_**](mf-topology-projectstop-attribute.md)                                   | Especifica o tempo de parada da topologia dentro do segmento atual, em unidades de 100 nanossegundos.                                                                                                                                              |
| [**STATUS DA \_ RESOLUÇÃO DE \_ \_ TOPOLOGIA DO MF**](mf-topology-resolution-status-attribute.md)                      | Especifica o status de uma tentativa de resolver uma topologia.                                                                                                                                                                          |
| [HORA DE INÍCIO DA TOPOLOGIA DO MF \_ \_ NA OPÇÃO \_ \_ \_ \_ APRESENTAÇÃO](mf-topology-start-time-on-presentation-switch.md) | Especifica a hora de início para apresentações na fila após a primeira apresentação.                                                                                                                                           |
| [OTIMIZAÇÕES DE \_ REPRODUÇÃO \_ ESTÁTICA DA \_ \_ TOPOLOGIA DO MF](mf-topology-static-playback-optimizations.md)           | Habilita otimizações estáticas no pipeline de vídeo.                                                                                                                                                                                |
| [Atributo MFT \_ FIELDOFUSE \_ UNLOCK \_](mft-fieldofuse-unlock-attribute.md)                                | Contém um [**ponteiro IMFFieldOfUseMFTUnlock,**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) que é usado para desbloquear um MFT com restrições de campo de uso. Para obter mais informações, consulte [Restrições de campo de uso.](field-of-use-restrictions.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> </dl>

 

 



