---
description: Descreve um buffer de índice.
ms.assetid: 5d45213e-b3c0-4eb7-a4f9-8d8730eb3899
title: Estrutura de D3DINDEXBUFFER_DESC (D3D9Types. h)
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
ms.openlocfilehash: 0a0bf63e732541f9394231cd82c23ff71a584b1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930624"
---
# <a name="d3dindexbuffer_desc-structure"></a>\_Estrutura desc de D3DINDEXBUFFER

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

Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato da superfície dos dados do buffer do índice.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Membro do tipo enumerado [**D3DRESOURCETYPE**](./d3dresourcetype.md) , identificando esse recurso como um buffer de índice.

</dd> <dt>

**Usage**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Combinação de um ou mais dos sinalizadores a seguir, especificando o uso desse recurso.



| Valor                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DUSAGE_DONOTCLIP"></span><span id="d3dusage_donotclip"></span><dl> <dt>**D3DUSAGE \_ DONOTCLIP**</dt> </dl>                            | Defina para indicar que o conteúdo do buffer de índice nunca exigirá o recorte.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_DYNAMIC"></span><span id="d3dusage_dynamic"></span><dl> <dt>**D3DUSAGE \_ dinâmico**</dt> </dl>                                  | Defina para indicar que o buffer de índice requer uso de memória dinâmica. Isso é útil para drivers porque permite que eles decidam onde posicionar o buffer. Em geral, os buffers de índice estáticos são colocados na memória de vídeo e os buffers de índice dinâmicos são colocados na memória AGP. Observe que não há nenhum uso estático separado; Se você não especificar D3DUSAGE \_ Dynamic, o buffer de índice se tornará estático. \_O D3DUSAGE Dynamic é estritamente imposto por meio dos \_ sinalizadores de bloqueio D3DLOCK descarte e D3DLOCK \_ NoOverwrite. Como resultado, D3DLOCK \_ descarte e D3DLOCK \_ NoOverwrite só são válidos em buffers de índice criados com D3DUSAGE \_ Dynamic; eles não são sinalizadores válidos em buffers de vértice estáticos.<br/> Para obter mais informações sobre como usar buffers de índice dinâmico, consulte [usando o vértice dinâmico e buffers de índice](performance-optimizations.md).<br/> Observe que D3DUSAGE \_ Dynamic não pode ser especificado em buffers de índice gerenciados. Para obter mais informações, consulte [Managing Resources (Direct3D 9)](managing-resources.md).<br/> |
| <span id="D3DUSAGE_RTPATCHES"></span><span id="d3dusage_rtpatches"></span><dl> <dt>**D3DUSAGE \_ RTPATCHES**</dt> </dl>                            | Defina para indicar quando o buffer de índice deve ser usado para desenhar primitivos de ordem alta.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DUSAGE_NPATCHES"></span><span id="d3dusage_npatches"></span><dl> <dt>**D3DUSAGE \_ NPATCHES**</dt> </dl>                               | Defina para indicar quando o buffer de índice deve ser usado para desenhar N patches.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_POINTS"></span><span id="d3dusage_points"></span><dl> <dt>**Pontos de D3DUSAGE \_**</dt> </dl>                                     | Defina para indicar quando o buffer de índice deve ser usado para sprites de ponto de desenho ou listas de pontos indexados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="D3DUSAGE_SOFTWAREPROCESSING"></span><span id="d3dusage_softwareprocessing"></span><dl> <dt>**D3DUSAGE \_ SOFTWAREPROCESSING**</dt> </dl> | Defina para indicar que o buffer deve ser usado com o processamento de software.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DUSAGE_WRITEONLY"></span><span id="d3dusage_writeonly"></span><dl> <dt>**\_WRITEONLY D3DUSAGE**</dt> </dl>                            | Informa ao sistema que o aplicativo grava somente no buffer de índice. O uso desse sinalizador permite que o driver escolha o melhor local de memória para operações de gravação e renderização eficientes. As tentativas de ler de um buffer de índice criado com esse recurso podem resultar em degradação do desempenho.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

**Pool**
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , especificando a classe de memória alocada para esse buffer de índice.

</dd> <dt>

**Tamanho**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamanho do buffer de índice, em bytes.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-getdesc)
</dt> <dt>

[Buffers de índice (Direct3D 9)](index-buffers.md)
</dt> </dl>

 

 
