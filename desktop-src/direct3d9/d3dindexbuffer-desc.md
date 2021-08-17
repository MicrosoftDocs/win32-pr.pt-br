---
description: Descreve um buffer de índice.
ms.assetid: 5d45213e-b3c0-4eb7-a4f9-8d8730eb3899
title: D3DINDEXBUFFER_DESC (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DINDEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a7a25e56ccb9877fad6b370f9ed81c6c7dcf0744a96734b1e17d6dc3abbc0535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804925"
---
# <a name="d3dindexbuffer_desc-structure"></a>Estrutura D3DINDEXBUFFER \_ DESC

Descreve um buffer de índice.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DINDEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
} D3DINDEXBUFFER_DESC, *LPD3DINDEXBUFFER_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**Formato**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Membro do tipo [enumerado D3DFORMAT,](d3dformat.md) descrevendo o formato de superfície dos dados do buffer de índice.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Membro do tipo [**enumerado D3DRESOURCETYPE,**](./d3dresourcetype.md) identificando esse recurso como um buffer de índice.

</dd> <dt>

**Usage**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Combinação de um ou mais dos sinalizadores a seguir, especificando o uso desse recurso.



| Valor                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DUSAGE_DONOTCLIP"></span><span id="d3dusage_donotclip"></span><dl> <dt>**D3DUSAGE \_ DONOTCLIP**</dt> </dl>                            | Definido para indicar que o conteúdo do buffer de índice nunca exigirá recorte.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_DYNAMIC"></span><span id="d3dusage_dynamic"></span><dl> <dt>**D3DUSAGE \_ DYNAMIC**</dt> </dl>                                  | Definido para indicar que o buffer de índice requer uso dinâmico de memória. Isso é útil para drivers porque permite que eles decidam onde colocar o buffer. Em geral, os buffers de índice estático são colocados na memória de vídeo e os buffers de índice dinâmico são colocados na memória AGP. Observe que não há nenhum uso estático separado; se você não especificar D3DUSAGE \_ DYNAMIC, o buffer de índice se tornou estático. D3DUSAGE DYNAMIC é imposto estritamente por meio dos sinalizadores de bloqueio \_ D3DLOCK DISCARD e \_ D3DLOCK \_ NOOVERWRITE. Como resultado, D3DLOCK DISCARD e D3DLOCK NOOVERWRITE são válidos apenas em buffers de índice criados com \_ D3DUSAGE DYNAMIC; eles não são sinalizadores válidos em buffers de vértice \_ \_ estáticos.<br/> Para obter mais informações sobre como usar buffers de índice dinâmico, consulte [Usando vértice dinâmico e buffers de índice.](performance-optimizations.md)<br/> Observe que D3DUSAGE \_ DYNAMIC não pode ser especificado em buffers de índice gerenciado. Para obter mais informações, [consulte Gerenciando recursos (Direct3D 9)](managing-resources.md).<br/> |
| <span id="D3DUSAGE_RTPATCHES"></span><span id="d3dusage_rtpatches"></span><dl> <dt>**D3DUSAGE \_ RTPATCHES**</dt> </dl>                            | Definido para indicar quando o buffer de índice deve ser usado para desenhar primitivos de ordem alta.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DUSAGE_NPATCHES"></span><span id="d3dusage_npatches"></span><dl> <dt>**D3DUSAGE \_ NPATCHES**</dt> </dl>                               | Definido para indicar quando o buffer de índice deve ser usado para desenhar N patches.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_POINTS"></span><span id="d3dusage_points"></span><dl> <dt>**PONTOS D3DUSAGE \_**</dt> </dl>                                     | Definido para indicar quando o buffer de índice deve ser usado para sprites de ponto de desenho ou listas de pontos indexados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="D3DUSAGE_SOFTWAREPROCESSING"></span><span id="d3dusage_softwareprocessing"></span><dl> <dt>**D3DUSAGE \_ SOFTWAREPROCESSING**</dt> </dl> | Definido para indicar que o buffer deve ser usado com o processamento de software.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DUSAGE_WRITEONLY"></span><span id="d3dusage_writeonly"></span><dl> <dt>**D3DUSAGE \_ WRITEONLY**</dt> </dl>                            | Informa ao sistema que o aplicativo grava somente no buffer de índice. Usar esse sinalizador permite que o driver escolha o melhor local de memória para operações de gravação e renderização eficientes. As tentativas de leitura de um buffer de índice que é criado com essa funcionalidade podem resultar em desempenho degradado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

**Pool**
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Membro do tipo [**enumerado D3DPOOL,**](./d3dpool.md) especificando a classe de memória alocada para esse buffer de índice.

</dd> <dt>

**Tamanho**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamanho do buffer de índice, em bytes.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-getdesc)
</dt> <dt>

[Buffers de índice (Direct3D 9)](index-buffers.md)
</dt> </dl>

 

 
