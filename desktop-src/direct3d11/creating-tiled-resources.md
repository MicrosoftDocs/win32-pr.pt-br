---
title: Criando recursos em ladrilhos
description: Os recursos em ladrilho são criados especificando- \_ \_ se o sinalizador de lado diverso do recurso D3D11 \_ ao criar um recurso.
ms.assetid: DED2B70C-1E95-4A85-A818-FD32165FBF6C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657fc2cca4d5c1d8fce9efba2013d3cd04291efc7f40d44b4ed325e40f843358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752576"
---
# <a name="creating-tiled-resources"></a>Criando recursos em ladrilhos

Os recursos em ladrilho são criados especificando-se o sinalizador de [**\_ \_ \_ lado diverso do recurso D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) ao criar um recurso.

Restrições sobre quando você pode usar [**o \_ recurso D3D11 de \_ \_ lado diverso**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) para criar um recurso são descritas em [parâmetros de criação de recursos lado a lado](tiled-resource-creation-parameters.md).

O armazenamento de um recurso que não é de lado de um é alocado no sistema de gráficos quando o recurso é criado. Por exemplo, quando você chama [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) para criar uma matriz de texturas 2D, o sistema de gráficos aloca armazenamento para essas texturas 2D. Quando um recurso ao lado do ladrilho é criado, o sistema de gráficos não aloca o armazenamento para o conteúdo do recurso. Em vez disso, quando um aplicativo cria um recurso de mosaico, o sistema de gráficos faz uma reserva de espaço de endereço apenas para a área da superfície do lado do ladrilho e, em seguida, permite que o mapeamento dos blocos seja controlado pelo aplicativo. O "mapeamento" de um bloco é simplesmente a localização física na memória para a qual um bloco lógico em um recurso aponta (ou **NULL** para um bloco não mapeado). Não confunda esse conceito com a noção de mapeamento de um recurso do Direct3D para acesso de CPU, que apesar de usar o mesmo nome é completamente independente. Você poderá definir e alterar o mapeamento de cada bloco individualmente, conforme necessário, sabendo que todos os blocos para uma superfície não precisam ser mapeadas de uma só vez, fazendo assim o uso eficaz da quantidade de memória disponível.

Esta seção fornece mais informações sobre como criar recursos ao lado.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Mapeamentos estão em um pool de blocos](mappings-are-into-a-tile-pool.md)<br/>                                     | Quando um recurso é criado com o sinalizador de [**\_ \_ \_ lado diverso do recurso D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) , os blocos que compõem o recurso são apontados em locais em um pool de peças. Um pool de blocos é um pool de memória (sustentado por uma ou mais alocações nos bastidores - nunca vistos pelo app). <br/> |
| [Parâmetros de criação de recursos por lado](tiled-resource-creation-parameters.md)<br/>                           | Há algumas restrições sobre o tipo de recursos do Direct3D que você pode criar com o sinalizador [**diD3D11 de \_ recursos \_ diversos \_ do recurso**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) . Esta seção fornece os parâmetros válidos para a criação de recursos em ladrilho.<br/>                                                |
| [Espaço de endereço disponível para recursos em ladrilho](address-space-available-for-tiled-resources.md)<br/>         | Esta seção especifica o espaço de endereço virtual que está disponível para recursos de lado. <br/>                                                                                                                                                                                                                           |
| [Parâmetros de criação de pool de blocos](tile-pool-creation-parameters.md)<br/>                                     | Use os parâmetros nesta seção para definir pools de blocos por meio da API [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) . <br/>                                                                                                                                                                              |
| [Processo cruzado de recursos cruzados e compartilhamento de dispositivos](tiled-resource-cross-process-and-device-sharing.md)<br/> | Os pools de bloco podem ser compartilhados com outros processos como recursos tradicionais. Os recursos de blocos gráficos que referenciam pools de bloco não podem ser compartilhados entre dispositivos e processos. Mas processos separados podem criar seus próprios recursos ao lado do bloco que são mapeados para pools de blocos que são compartilhados entre esses recursos de lado. <br/>          |
| [Operações disponíveis em recursos ao lado](operations-available-on-tiled-resources.md)<br/>                 | Esta seção lista as operações que você pode executar em recursos de lado.<br/>                                                                                                                                                                                                                                             |
| [Operações disponíveis em pools de blocos](operations-available-on-tile-pools.md)<br/>                           | Esta seção lista as operações que você pode executar em pools de blocos.<br/>                                                                                                                                                                                                                                                  |
| [Como a área de um recurso do lado do ladrilho é colocada](how-a-tiled-resource-s-area-is-tiled.md)<br/>                       | Quando você cria um recurso de mosaico, as dimensões, o tamanho do elemento de formato e o número de fatias de mipmaps e/ou matrizes (se aplicável) determinam o número de blocos necessários para fazer o fallback da área de superfície inteira. <br/>                                                                                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos em ladrilho](tiled-resources.md)
</dt> </dl>

 

 





