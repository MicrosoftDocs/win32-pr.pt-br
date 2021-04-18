---
description: 'Lista as consultas para o método IDirect3DAuthenticatedChannel9:: Query.'
ms.assetid: 75e246c6-bf23-44d9-8fb3-46a6dc5324a5
title: Consultas de Proteção de Conteúdo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a72f7f054783a644cb352727f4bf65864bf5f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791259"
---
# <a name="content-protection-queries"></a>Consultas de Proteção de Conteúdo

Lista as consultas para o método [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .



| Solicitação de status                                                                                                                            | Descrição                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Acessibilidade D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-accessibilityattributes.md)                                   | Retorna o tipo de barramento de e/s usado para enviar dados para a GPU.                                                                                                   |
| [**\_Canaltype D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-channeltype.md)                                                           | Retorna o tipo de canal autenticado.                                                                                                                  |
| [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md)                                                       | Retorna identificadores para a sessão de criptografia e para o dispositivo Direct3D que estão associados a um dispositivo de decodificador de vídeo do DirectX 2 (DXVA-2) especificado. |
| [**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedquery-currentencryptionwhenaccessible.md)                   | Retorna o tipo de criptografia que é aplicado antes que o conteúdo se torne acessível à CPU ou ao barramento.                                                            |
| [**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md)                                                         | Retorna um identificador para o dispositivo que está associado a este canal autenticado.                                                                          |
| [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md)                         | Retorna um dos tipos de criptografia que podem ser usados para criptografar o conteúdo antes que ele se torne acessível à CPU ou ao barramento.                                     |
| [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md)               | Retorna o número de tipos de criptografia que podem ser usados para criptografar o conteúdo antes que ele se torne acessível à CPU ou ao barramento.                                  |
| [**Saída de D3DAUTHENTICATEDQUERY \_**](d3dauthenticatedquery-outputid.md)                                                                 | Retorna um dos identificadores de saída associados a uma sessão criptográfica especificada e ao dispositivo Direct3D.                                        |
| [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md)                                                       | Retorna o número de identificadores de saída associados a uma sessão criptográfica especificada e ao dispositivo Direct3D.                                             |
| [**Proteção do D3DAUTHENTICATEDQUERY \_**](d3dauthenticatedquery-protection.md)                                                             | Retorna o nível de proteção atual para o dispositivo.                                                                                                        |
| [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md)                   | Retorna informações sobre um processo que tem permissão para abrir recursos compartilhados com acesso restrito.                                                        |
| [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md)         | Retorna o número de processos que têm permissão para abrir recursos compartilhados com acesso restrito.                                                           |
| [**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) | Retorna o número de recursos compartilhados protegidos que podem ser abertos por qualquer processo sem restrições.                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs de vídeo do Direct3D](direct3d-video-apis.md)
</dt> <dt>

[Proteção de Conteúdo baseado em GPU](gpu-based-content-protection.md)
</dt> </dl>

 

 



