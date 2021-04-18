---
description: Descreve as estruturas usadas pelas interfaces de vídeo do Microsoft Direct3D 9.
ms.assetid: 584c087e-53f0-42d8-99ed-a0d013379363
title: Estruturas de vídeo do Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ac8e03ff524f7f943c6adbee39b57785112a3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810741"
---
# <a name="direct3d-9-video-structures"></a>Estruturas de vídeo do Direct3D 9

Descreve as estruturas usadas pelas interfaces de vídeo do Microsoft Direct3D 9.



| Estrutura                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OMAC do D3D \_**](d3d-omac.md)<br/> Contém um Message Authentication Code (MAC).<br/>                                                                                                                                                                                                                                                                        |
| [**D3DAES \_ CTR \_ IV**](d3daes-ctr-iv.md)<br/> Contém um vetor de inicialização (IV).<br/>                                                                                                                                                                                                                                                                   |
| [**D3DAUTHENTICATEDCHANNEL \_ Configurar a \_ entrada**](d3dauthenticatedchannel-configure-input.md)<br/> Contém dados de entrada para o método [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .<br/>                                                                                                                     |
| [**D3DAUTHENTICATEDCHANNEL \_ Configurar \_ saída**](d3dauthenticatedchannel-configure-output.md)<br/> Contém a resposta a uma chamada para o método [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .<br/>                                                                                                        |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREINITIALIZE**](d3dauthenticatedchannel-configureinitialize.md)<br/> Contém dados de entrada para um comando de [**\_ inicialização D3DAUTHENTICATEDCONFIGURE**](d3dauthenticatedconfigure-initialize.md) .<br/>                                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREPROTECTION**](d3dauthenticatedchannel-configureprotection.md)<br/> Contém dados de entrada para um comando de [**\_ proteção D3DAUTHENTICATEDCONFIGURE**](d3dauthenticatedconfigure-protection.md) .<br/>                                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md)<br/> Contém dados de entrada para um comando [**D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) .<br/>                                                                                                           |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURESHAREDRESOURCE**](d3dauthenticatedchannel-configuresharedresource.md)<br/> Contém dados de entrada para um comando [**D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) .<br/>                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREUNCOMPRESSEDENCRYPTION**](d3dauthenticatedchannel-configureuncompressedencryption.md)<br/> Contém dados de entrada para um comando [**D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) .<br/>                                                                   |
| [**\_Sinalizadores de proteção do D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-protection-flags.md)<br/> Especifica o nível de proteção para conteúdo de vídeo.<br/>                                                                                                                                                                                                   |
| [**\_Entrada de consulta D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-query-input.md)<br/> Contém dados de entrada para o método [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .<br/>                                                                                                                                     |
| [**\_Saída de consulta D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-query-output.md)<br/> Contém a resposta a uma chamada para o método [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .<br/>                                                                                                                        |
| [**\_Saída D3DAUTHENTICATEDCHANNEL QUERYCHANNELTYPE \_**](d3dauthenticatedchannel-querychanneltype-output.md)<br/> Contém a resposta a uma [**consulta \_ channelType D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-channeltype.md) .<br/>                                                                                                                     |
| [**\_Entrada D3DAUTHENTICATEDCHANNEL QUERYCRYPTOSESSION \_**](d3dauthenticatedchannel-querycryptosession-input.md)<br/> Contém dados de entrada para uma consulta [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) .<br/>                                                                                                                |
| [**\_Saída D3DAUTHENTICATEDCHANNEL QUERYCRYPTOSESSION \_**](d3dauthenticatedchannel-querycryptosession-output.md)<br/> Contém a resposta a uma consulta [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) .<br/>                                                                                                             |
| [**\_Saída D3DAUTHENTICATEDCHANNEL QUERYDEVICEHANDLE \_**](d3dauthenticatedchannel-querydevicehandle-output.md)<br/> Contém a resposta a uma consulta [**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) .<br/>                                                                                                                 |
| [**\_Entrada D3DAUTHENTICATEDCHANNEL QUERYEVICTIONENCRYPTIONGUID \_**](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)<br/> Contém dados de entrada para uma consulta [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .<br/>                                                                |
| [**\_Saída D3DAUTHENTICATEDCHANNEL QUERYEVICTIONENCRYPTIONGUID \_**](d3dauthenticatedchannel-queryevictionencryptionguid-output.md)<br/> Contém a resposta a uma consulta [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .<br/>                                                             |
| [**\_Saída D3DAUTHENTICATEDCHANNEL QUERYEVICTIONENCRYPTIONGUIDCOUNT \_**](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md)<br/> Contém a resposta a uma consulta [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md) .<br/>                                         |
| [**\_Saída D3DAUTHENTICATEDCHANNEL QUERYINFOBUSTYPE \_**](d3dauthenticatedchannel-queryinfobustype-output.md)<br/> Contém a resposta a uma [**consulta \_ accessibilityattributes do D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-accessibilityattributes.md) .<br/>                                                                                             |
| [**\_Entrada D3DAUTHENTICATEDCHANNEL QUERYOUTPUTID \_**](d3dauthenticatedchannel-queryoutputid-input.md)<br/> Contém dados de Intput para uma consulta de [**\_ saída de D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-outputid.md) .<br/>                                                                                                                                   |
| [**\_Saída D3DAUTHENTICATEDCHANNEL QUERYOUTPUTID \_**](d3dauthenticatedchannel-queryoutputid-output.md)<br/> Contém a resposta a uma [**consulta \_ outputid D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-outputid.md) .<br/>                                                                                                                                 |
| [**\_Entrada D3DAUTHENTICATEDCHANNEL QUERYOUTPUTIDCOUNT \_**](d3dauthenticatedchannel-queryoutputidcount-input.md)<br/> Contém dados de entrada para uma consulta [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) .<br/>                                                                                                                |
| [**\_Saída D3DAUTHENTICATEDCHANNEL QUERYOUTPUTIDCOUNT \_**](d3dauthenticatedchannel-queryoutputidcount-output.md)<br/> Contém a resposta a uma consulta [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) .<br/>                                                                                                             |
| [**\_Saída D3DAUTHENTICATEDCHANNEL QUERYPROTECTION \_**](d3dauthenticatedchannel-queryprotection-output.md)<br/> Contém a resposta a uma consulta de [**\_ proteção D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-protection.md) .<br/>                                                                                                                         |
| [**\_Entrada D3DAUTHENTICATEDCHANNEL QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-input.md)<br/> Contém dados de entrada para uma consulta [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .<br/>                                        |
| [**\_Saída D3DAUTHENTICATEDCHANNEL QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md)<br/> Contém a resposta a uma consulta [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .<br/>                                     |
| [**\_Saída D3DAUTHENTICATEDCHANNEL QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT \_**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocesscount-output.md)<br/> Contém a resposta a uma consulta [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) .<br/>                 |
| [**\_Saída D3DAUTHENTICATEDCHANNEL QUERYUNCOMPRESSEDENCRYPTIONLEVEL \_**](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md)<br/> Contém a resposta a uma consulta [**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedquery-currentencryptionwhenaccessible.md) .<br/>                                             |
| [**\_Saída D3DAUTHENTICATEDCHANNEL QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT \_**](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md)<br/> Contém a resposta a uma consulta [**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) .<br/> |
| [**D3DCONTENTPROTECTIONCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps)<br/> Descreve os recursos de proteção de conteúdo de um driver de vídeo.<br/>                                                                                                                                                                                                                    |
| [**\_Informações do bloco D3DENCRYPTED \_**](d3dencrypted-block-info.md)<br/> Especifica quais bytes são criptografados em uma superfície de vídeo protegida.<br/>                                                                                                                                                                                                                     |
| [**D3DOVERLAYCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3doverlaycaps)<br/> Especifica os recursos de sobreposição de hardware para um dispositivo Direct3D.<br/>                                                                                                                                                                                                                                            |
| [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo)<br/> Especifica um buffer para o método [**IDirect3DDXVADevice9:: execute**](idirect3ddxvadevice9-execute.md) .<br/>                                                                                                                                                                                                  |
| [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo)<br/> Especifica os requisitos para superfícies compactadas para a DXVA (aceleração de vídeo do DirectX).<br/>                                                                                                                                                                                                         |
| [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo)<br/> Especifica as dimensões e o formato de pixel das superfícies descompactadas para decodificação de vídeo DXVA.<br/>                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs de vídeo do Direct3D](direct3d-video-apis.md)
</dt> </dl>

 

 




