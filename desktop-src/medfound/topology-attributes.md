---
description: Atributos de topologia
ms.assetid: 50102096-a29f-4c00-a685-179ba5d71089
title: Atributos de topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 286b6dbfe922461083b49d77ad2351e98d562d3b
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "105753626"
---
# <a name="topology-attributes"></a>Atributos de topologia

Os atributos a seguir se aplicam a topologias.



| Atributo                                                                                                | Descrição                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_modo de \_ DXVA da topologia MF \_](mf-topology-dxva-mode.md)                                                    | Especifica se o carregador de topologia permite o DXVA (Microsoft DirectX Video Acceleration) na topologia.                                                                                                                         |
| [\_alteração dinâmica de topologia MF \_ \_ \_ não \_ permitida](mf-topology-dynamic-change-not-allowed.md)                | Especifica se a sessão de mídia tenta modificar a topologia quando o formato de um fluxo é alterado.                                                                                                                           |
| [\_topologia MF \_ habilitar \_ XVP \_ para \_ reprodução](mf-topology-enable-xvp-for-playback.md)                | Especifica se o carregador de topologia habilita o processador de vídeo transcodificar (XVP). para conversões, habilitando a conversão de cores acelerada por hardware.                                                                                        |
| [\_tipos de \_ origem enumerar topologia \_ MF \_](mf-topology-enumerate-source-types.md)                         | Especifica se o carregador de topologia enumera os tipos de mídia fornecidos pela origem da mídia.                                                                                                                                     |
| [\_modo de \_ hardware de topologia MF \_](mf-topology-hardware-mode.md)                                            | Especifica se as transformações baseadas em hardware devem ser incluídas na topologia.                                                                                                                                                            |
| [**\_topologia MF \_ sem \_ marca de marcação \_**](mf-topology-no-markin-markout-attribute.md)                     | Especifica se o pipeline apara amostras.                                                                                                                                                                                      |
| [\_taxa de \_ quadros de reprodução da topologia MF \_](mf-topology-playback-framerate.md)                                  | Especifica a taxa de atualização do monitor.                                                                                                                                                                                                |
| [\_ \_ esmaecimento máximo da reprodução da topologia MF \_ \_](mf-topology-playback-max-dims.md)                                   | Especifica o tamanho da janela de destino para reprodução de vídeo.                                                                                                                                                                   |
| [**\_PROJECTSTART de topologia MF \_**](mf-topology-projectstart-attribute.md)                                 | Especifica a hora de início da topologia dentro do segmento atual, em unidades de 100 a nanossegundos.                                                                                                                                             |
| [**\_PROJECTSTOP de topologia MF \_**](mf-topology-projectstop-attribute.md)                                   | Especifica a hora de parada da topologia dentro do segmento atual, em unidades de 100 a nanossegundos.                                                                                                                                              |
| [**\_status de \_ resolução da topologia MF \_**](mf-topology-resolution-status-attribute.md)                      | Especifica o status de uma tentativa de resolver uma topologia.                                                                                                                                                                          |
| [\_ \_ \_ hora de início da topologia MF \_ na \_ opção de apresentação \_](mf-topology-start-time-on-presentation-switch.md) | Especifica a hora de início para as apresentações que são enfileiradas após a primeira apresentação.                                                                                                                                           |
| [\_ \_ \_ otimizações de reprodução \_ estática da topologia MF](mf-topology-static-playback-optimizations.md)           | Habilita otimizações estáticas no pipeline de vídeo.                                                                                                                                                                                |
| [\_Atributo de \_ desbloqueio de FIELDOFUSE MFT \_](mft-fieldofuse-unlock-attribute.md)                                | Contém um ponteiro [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , que é usado para desbloquear um MFT com restrições de campo de uso. Para obter mais informações, consulte [campo de restrições de uso](field-of-use-restrictions.md). |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> </dl>

 

 



