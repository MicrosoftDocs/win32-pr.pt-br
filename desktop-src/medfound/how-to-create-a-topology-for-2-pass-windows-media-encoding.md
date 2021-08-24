---
description: os modos de codificação de duas passagens têm suporte em determinados Windows codificadores de mídia e Media Foundation na camada de pipeline.
ms.assetid: 3fd5baff-142f-453e-bb97-b355ee6678fc
title: como criar uma topologia para Two-Pass Windows codificação de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525a98faa424371f2d80739e5c68f199cfc7ed6443c25ab3d15b575afdd003e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724876"
---
# <a name="how-to-create-a-topology-for-two-pass-windows-media-encoding"></a>como criar uma topologia para Two-Pass Windows codificação de mídia

os modos de codificação de duas passagens têm suporte em determinados Windows codificadores de mídia e Media Foundation na camada de pipeline. O aplicativo deve configurar e configurar a topologia de codificação semelhante àquela na codificação de passagem única, mas no modo de codificação de duas passagens, o aplicativo deve executar a sessão de codificação duas vezes. Na primeira passagem, o codificador reúne informações sobre o conteúdo do fluxo. Na segunda passagem, usando as informações coletadas na primeira passagem, o arquivo de saída final é gerado. Ao processar os exemplos para o fluxo duas vezes, a codificação de duas passagens otimiza o processo de codificação e produz arquivos codificados com maior qualidade. Modos de codificação de duas passagens não podem ser usados em fluxos ao vivo.

O Media Foundation dá suporte aos seguintes modos de codificação de duas passagens:

-   [Codificação de taxa de bits variável irrestrita](unconstrained-variable-bit-rate--vbr--encoding.md)
-   [Codificação de taxa de bits de variável com restrição de pico](peak-constrained-variable-bit-rate--vbr--encoding.md)

A criação de uma topologia de codificação para codificação de duas passagens é semelhante a modos de passagem única. A lista a seguir mostra as principais diferenças.

-   A configuração do codificador deve incluir a propriedade [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md) definida como 2 e a propriedade [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) como Variant \_ true. Isso filtra os recursos do codificador para modos de duas passagens. Se você estiver usando objetos de ativação, passe essas propriedades para [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) ou [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).
-   Para a primeira passagem, use um coletor de mídia fictício no nó de saída porque os exemplos gerados nessa passagem não são adicionados ao arquivo final.
-   Para a segunda passagem, consulte o codificador para as propriedades de pós-codificação necessárias e substitua o nó do coletor de mídia fictício pelo coletor de mídia do ASF por essas propriedades definidas.

para obter mais informações sobre como configurar uma topologia de codificação, consulte [Tutorial: passagem única Windows codificação de mídia](tutorial--1-pass-windows-media-encoding.md).

o procedimento a seguir resume as etapas de codificação Windows conteúdo de mídia em um contêiner ASF usando um modo de codificação de duas passagens.

1.  Crie uma origem de mídia para o especificado usando o resolvedor de origem.
2.  Enumere os fluxos na origem da mídia.
3.  Crie o coletor de mídia ASF e adicione coletores de fluxo dependendo dos fluxos na origem de mídia que precisam ser codificados.
4.  Crie o coletor de mídia.
5.  crie os codificadores de mídia Windows para os fluxos no arquivo de saída.
6.  Configure os codificadores com as propriedades de codificação de 2 passagens.
7.  Crie uma topologia de codificação parcial conectando a origem, os codificadores e o coletor de mídia.
8.  Crie uma instância da sessão de mídia e defina a topologia na sessão de mídia.
9.  Execute a primeira passagem de codificação controlando a sessão de mídia e obtendo todos os eventos relevantes da sessão de mídia.
10. Feche e desligue a sessão de codificação.
11. Consulte o codificador para as seguintes propriedades, dependendo do tipo de codificação: 

    | Tipo de codificação                                                                                        | Nome da propriedade                                                                                                                                                                                                                                                                                                                                                     |
    |------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [Codificação de taxa de bits variável irrestrita](unconstrained-variable-bit-rate--vbr--encoding.md)       | [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md)<br/> [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)<br/> [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md)<br/> [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md)<br/>                                                                                                               |
    | [Codificação de taxa de bits de variável com restrição de pico](peak-constrained-variable-bit-rate--vbr--encoding.md) | [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md)<br/> [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)<br/> [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md)<br/> [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md)<br/> [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md)<br/> [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md)<br/> |

    

     

12. Crie o coletor de arquivo ASF e adicione os coletores de fluxo necessários dependendo dos fluxos que você deseja incluir no arquivo de saída final.
13. Defina as propriedades do codificador recuperadas na etapa 11 no coletor de arquivos.
14. Substitua o coletor de mídia no nó de saída pelo coletor de arquivos recém-criado.
15. Crie uma instância da sessão de mídia e defina a topologia atualizada na sessão de mídia.
16. Execute a segunda passagem de codificação controlando a sessão de mídia e obtendo todos os eventos relevantes da sessão de mídia.
17. Aguarde o evento [MEEndOfPresentation](meendofpresentation.md) da sessão de mídia e, no manipulador de eventos, obtenha os valores de propriedade de codificação do codificador e defina-os no coletor de arquivos. para obter mais informações, consulte "atualizar propriedades de codificação no coletor de arquivos", no [Tutorial: passagem única Windows codificação de mídia](tutorial--1-pass-windows-media-encoding.md).
18. Feche e desligue a sessão de codificação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Componentes ASF da camada de pipeline](pipeline-layer-asf-components.md)
</dt> </dl>

 

 




