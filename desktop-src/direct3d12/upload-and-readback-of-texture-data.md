---
title: Carregando dados de textura por meio de buffers
description: Carregar dados de textura 2D ou 3D é semelhante a carregar dados 1D, exceto que os aplicativos precisam prestar mais atenção ao alinhamento de dados relacionado à densidade da linha.
ms.assetid: 22A25A94-A45C-482D-853A-FA6860EE7E4E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c095d93237a44369cb249d6de9e514fa7021a91fb78430ddc428c88e4e71b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027986"
---
# <a name="uploading-texture-data-through-buffers"></a>Carregando dados de textura por meio de buffers

Carregar dados de textura 2D ou 3D é semelhante a carregar dados 1D, exceto que os aplicativos precisam prestar mais atenção ao alinhamento de dados relacionado à densidade da linha. Os buffers podem ser usados de forma ortogonal e simultânea de várias partes do pipeline de gráficos e são muito flexíveis.

-   [Upload Dados de textura por meio de buffers](#upload-texture-data-via-buffers)
-   [Copia](#copying)
-   [Mapeamento e desmapeamento](#mapping-and-unmapping)
-   [Alinhamento do buffer](#buffer-alignment)
-   [Tópicos relacionados](#related-topics)

## <a name="upload-texture-data-via-buffers"></a>Upload Dados de textura por meio de buffers

Os aplicativos devem carregar dados por meio de [**ID3D12GraphicsCommandList:: CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) ou [**ID3D12GraphicsCommandList:: CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion). É muito mais provável que os dados de textura sejam maiores, acessados repetidamente e se beneficiem da coerência de cache aprimorada de layouts de memória não linear do que outros dados de recurso. Quando os buffers são usados no D3D12, os aplicativos têm controle total sobre o posicionamento de dados e a organização associada à cópia de dados de recurso, desde que os requisitos de alinhamento de memória sejam atendidos.

O exemplo destaca onde o aplicativo simplesmente achata os dados 2D em 1D antes de colocá-los no buffer. Para o cenário mipmap 2D, o aplicativo pode mesclar cada subrecurso discretamente e usar rapidamente um algoritmo de subalocação 1D ou usar uma técnica de subalocação 2D mais complicada para minimizar a utilização da memória de vídeo. Espera-se que a primeira técnica seja usada com mais frequência, pois é mais simples. A segunda técnica pode ser útil ao empacotar dados em um disco ou em uma rede. Em ambos os casos, o aplicativo ainda deve chamar as APIs de cópia para cada subrecurso.

```cpp
// Prepare a pBitmap in memory, with bitmapWidth, bitmapHeight, and pixel format of DXGI_FORMAT_B8G8R8A8_UNORM. 
//
// Sub-allocate from the buffer for texture data.
//

D3D12_SUBRESOURCE_FOOTPRINT pitchedDesc = { 0 };
pitchedDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
pitchedDesc.Width = bitmapWidth;
pitchedDesc.Height = bitmapHeight;
pitchedDesc.Depth = 1;
pitchedDesc.RowPitch = Align(bitmapWidth * sizeof(DWORD), D3D12_TEXTURE_DATA_PITCH_ALIGNMENT);

//
// Note that the helper function UpdateSubresource in D3DX12.h, and ID3D12Device::GetCopyableFootprints 
// can help applications fill out D3D12_SUBRESOURCE_FOOTPRINT and D3D12_PLACED_SUBRESOURCE_FOOTPRINT structures.
//
// Refer to the D3D12 Code example for the previous section "Uploading Different Types of Resources"
// for the code for SuballocateFromBuffer.
//

SuballocateFromBuffer(
    pitchedDesc.Height * pitchedDesc.RowPitch,
    D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT
    );

D3D12_PLACED_SUBRESOURCE_FOOTPRINT placedTexture2D = { 0 };
placedTexture2D.Offset = m_pDataCur – m_pDataBegin;
placedTexture2D.Footprint = pitchedDesc;

//
// Copy texture data from DWORD* pBitmap->pixels to the buffer
//

for (UINT y = 0; y < bitmapHeight; y++)
{
  UINT8 *pScan = m_pDataBegin + placedTexture2D.Offset + y * pitchedDesc.RowPitch;
  memcpy( pScan, &(pBitmap->pixels[y * bitmapWidth]), sizeof(DWORD) * bitmapWidth );
}

//
// Create default texture2D resource.
//

D3D12_RESOURCE_DESC  textureDesc { ... };

CComPtr<ID3D12Resource> texture2D;
d3dDevice->CreateCommittedResource( 
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT), 
        D3D12_HEAP_FLAG_NONE, &textureDesc, 
        D3D12_RESOURCE_STATE_COPY_DEST, 
        nullptr, 
        IID_PPV_ARGS(&texture2D) );

//
// Copy heap data to texture2D.
//

commandList->CopyTextureRegion( 
        &CD3DX12_TEXTURE_COPY_LOCATION( texture2D, 0 ), 
        0, 0, 0, 
        &CD3DX12_TEXTURE_COPY_LOCATION( m_spUploadHeap, placedTexture2D ), 
        nullptr );
```

Observe o uso das estruturas auxiliares [**CD3DX12 \_ heap de \_ Propriedades**](cd3dx12-heap-properties.md) e [**\_ \_ \_ local de cópia de textura CD3DX12**](cd3dx12-texture-copy-location.md)e os métodos [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) e [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).

## <a name="copying"></a>Copiando

Os métodos D3D12 permitem que os aplicativos substituam os dados de D3D11 [**UpdateSubresource**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion)e Resource inicial. Um único subrecurso 3D digno de dados de textura de linha principal pode estar localizado em recursos de buffer. [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) pode copiar esses dados de textura do buffer para um recurso de textura com um layout de textura desconhecido e vice-versa. Os aplicativos devem preferir esse tipo de técnica para popular os recursos de GPU acessados com frequência, criando buffers grandes em um heap de carregamento ao criar os recursos de GPU acessados com frequência em um heap padrão que não tem acesso à CPU. Uma técnica tão eficientemente dá suporte a GPUs discretas e a suas grandes quantidades de memória inacessível por CPU, sem o uso comum de arquiteturas de uma.

Observe as duas constantes a seguir:

```cpp
const UINT D3D12_TEXTURE_DATA_PITCH_ALIGNMENT = 256;
const UINT D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT = 512;
```

-   [**\_Superfície do SUBrecurso do D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
-   [**D3D12 \_ colocou a \_ superfície do subrecurso \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)
-   [**\_Local de \_ cópia de textura D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
-   [**\_Tipo de \_ cópia de textura D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)
-   [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
-   [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**ID3D12GraphicsCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**ID3D12CommandQueue::UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)

## <a name="mapping-and-unmapping"></a>Mapeamento e desmapeamento

[**Mapear**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) e cancelar o [**mapeamento**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) podem ser chamados por vários threads com segurança. A primeira chamada para **MAP** aloca um intervalo de endereços virtuais de CPU para o recurso. A última chamada para o **mapeamento** Desaloca o intervalo de endereços virtuais da CPU. O endereço virtual da CPU é normalmente retornado para o aplicativo.

Sempre que os dados são passados entre a CPU e a GPU por meio de recursos em heaps readback, o [**MAP**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) e o [**mapeamento**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) devem ser usados para dar suporte a todos os sistemas D3D12 com suporte no. Manter os intervalos o mais rígido possível maximiza a eficiência nos sistemas que exigem intervalos (consulte o [**\_ intervalo de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).

O desempenho das ferramentas de depuração beneficia-se não apenas do uso preciso de intervalos em todas as chamadas de mapeamento de [**mapa**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)  /  [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) , mas também de aplicativos desmapeando recursos quando as modificações de CPU não forem mais feitas.

O método D3D11 do uso de [**MAP**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (com o conjunto de parâmetros de descarte) para renomear recursos não tem suporte em D3D12. Os aplicativos devem implementar a renomeação de recursos em si. Todas as chamadas de **mapa** são implicitamente sem \_ substituição e multi-threaded. É responsabilidade do aplicativo garantir que qualquer trabalho de GPU relevante contido nas listas de comandos seja concluído antes de acessar os dados com a CPU. As chamadas D3D12 para **MAP** não liberam implicitamente nenhum buffer de comando, nem bloqueiam a espera do trabalho de conclusão da GPU. Como resultado, o **mapeamento** e o [**desmapeamento**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) podem até mesmo ser otimizados em alguns cenários.

## <a name="buffer-alignment"></a>Alinhamento do buffer

Restrições de alinhamento de buffer:

-   A cópia linear de subrecurso deve estar alinhada a 512 bytes (com a densidade de linha alinhada aos \_ bytes de alinhamento de densidade de dados de textura D3D12 \_ \_ \_ ).
-   As leituras de dados constantes devem ser um múltiplo de 256 bytes do início do heap (ou seja, somente de endereços que são de 256 bytes alinhados).
-   As leituras de dados de índice devem ser um múltiplo do tamanho do tipo de dados de índice (ou seja, somente de endereços que são naturalmente alinhados para os dados).
-   Os dados [**ID3D12GraphicsCommandList:: ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) devem ser de deslocamentos que são múltiplos de 4 (ou seja, somente de endereços que são alinhados em DWORD).

## <a name="related-topics"></a>Tópicos relacionados

* [Subalocação em buffers](large-buffers.md)
