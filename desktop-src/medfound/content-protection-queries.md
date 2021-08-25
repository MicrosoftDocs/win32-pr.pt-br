---
description: Lista as consultas para o método IDirect3DAuthenticatedChannel9::Query.
ms.assetid: 75e246c6-bf23-44d9-8fb3-46a6dc5324a5
title: Proteção de Conteúdo consultas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c5aaa8c43cf722d13550ab4a1860e7a53780e7e82da7f374e28a7f599a22638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829086"
---
# <a name="content-protection-queries"></a>Proteção de Conteúdo consultas

Lista as consultas para o [**método IDirect3DAuthenticatedChannel9::Query.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)



| Solicitação de status                                                                                                                            | Descrição                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md)                                   | Retorna o tipo de barramento de E/S usado para enviar dados para a GPU.                                                                                                   |
| [**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**](d3dauthenticatedquery-channeltype.md)                                                           | Retorna o tipo de canal autenticado.                                                                                                                  |
| [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md)                                                       | Retorna os handles para a sessão criptográfica e o dispositivo Direct3D associados a um dispositivo decodificador DXVA-2 (Aceleração de Vídeo DirectX 2) especificado. |
| [**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedquery-currentencryptionwhenaccessible.md)                   | Retorna o tipo de criptografia que é aplicado antes que o conteúdo se torne acessível para a CPU ou o barramento.                                                            |
| [**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md)                                                         | Retorna um alça para o dispositivo associado a esse canal autenticado.                                                                          |
| [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md)                         | Retorna um dos tipos de criptografia que podem ser usados para criptografar conteúdo antes que ele se torne acessível para a CPU ou o barramento.                                     |
| [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md)               | Retorna o número de tipos de criptografia que podem ser usados para criptografar conteúdo antes que ele se torne acessível para a CPU ou o barramento.                                  |
| [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md)                                                                 | Retorna um dos identificadores de saída associados a uma sessão criptográfica especificada e ao dispositivo Direct3D.                                        |
| [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md)                                                       | Retorna o número de identificadores de saída associados a uma sessão de criptografia especificada e ao dispositivo Direct3D.                                             |
| [**PROTEÇÃO D3DAUTHENTICATEDQUERY \_**](d3dauthenticatedquery-protection.md)                                                             | Retorna o nível de proteção atual para o dispositivo.                                                                                                        |
| [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md)                   | Retorna informações sobre um processo que tem permissão para abrir recursos compartilhados com acesso restrito.                                                        |
| [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md)         | Retorna o número de processos que têm permissão para abrir recursos compartilhados com acesso restrito.                                                           |
| [**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) | Retorna o número de recursos compartilhados protegidos que podem ser abertos por qualquer processo sem restrições.                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs de vídeo do Direct3D](direct3d-video-apis.md)
</dt> <dt>

[Dados baseados em GPU Proteção de Conteúdo](gpu-based-content-protection.md)
</dt> </dl>

 

 



