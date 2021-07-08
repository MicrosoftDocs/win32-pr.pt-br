---
description: Identifica o tipo de consulta.
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: Enumeração D3DQUERYTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DQUERYTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0778e879a6147c185964808ee4b4c302bd211ef3
ms.sourcegitcommit: bfab92e16614d4fa54b044917358261232bda81a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/08/2021
ms.locfileid: "113489690"
---
# <a name="d3dquerytype-enumeration"></a>Enumeração D3DQUERYTYPE

Identifica o tipo de consulta. Para obter informações sobre consultas, consulte [consultas (Direct3D 9)](queries.md)

## <a name="syntax"></a>Sintaxe


```C++
typedef enum D3DQUERYTYPE { 
  D3DQUERYTYPE_VCACHE             = 4,
  D3DQUERYTYPE_RESOURCEMANAGER    = 5,
  D3DQUERYTYPE_VERTEXSTATS        = 6,
  D3DQUERYTYPE_EVENT              = 8,
  D3DQUERYTYPE_OCCLUSION          = 9,
  D3DQUERYTYPE_TIMESTAMP          = 10,
  D3DQUERYTYPE_TIMESTAMPDISJOINT  = 11,
  D3DQUERYTYPE_TIMESTAMPFREQ      = 12,
  D3DQUERYTYPE_PIPELINETIMINGS    = 13,
  D3DQUERYTYPE_INTERFACETIMINGS   = 14,
  D3DQUERYTYPE_VERTEXTIMINGS      = 15,
  D3DQUERYTYPE_PIXELTIMINGS       = 16,
  D3DQUERYTYPE_BANDWIDTHTIMINGS   = 17,
  D3DQUERYTYPE_CACHEUTILIZATION   = 18,
  D3DQUERYTYPE_MEMORYPRESSURE     = 19
} D3DQUERYTYPE, *LPD3DQUERYTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE \_ VCACHE**
</dt> <dd>

Consulte Dicas de driver sobre o layout de dados para o cache de vértice.

</dd> <dt>

<span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**\_RESOURCEMANAGER D3DQUERYTYPE**
</dt> <dd>

Consulte o Gerenciador de recursos. Para essa consulta, os sinalizadores de comportamento do dispositivo devem incluir [D3DCREATE \_ desabilitar o \_ \_ Gerenciamento de driver](d3dcreate.md).

</dd> <dt>

<span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE \_ VERTEXSTATS**
</dt> <dd>

Estatísticas de vértice da consulta.

</dd> <dt>

<span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**\_Evento D3DQUERYTYPE**
</dt> <dd>

Consultar qualquer e todos os eventos assíncronos que foram emitidos de chamadas de API.

</dd> <dt>

<span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE \_ oclusão**
</dt> <dd>

Uma consulta oclusão retorna o número de pixels que passam testes em z. Esses pixels são para primitivos desenhados entre o problema de [**D3DISSUE \_ begin**](d3dissue-begin.md) e [**D3DISSUE \_ end**](d3dissue-end.md). Isso permite que um aplicativo Verifique o resultado do oclusão em relação a 0. Zero é totalmente obstruído, o que significa que os pixels não são visíveis na posição atual da câmera.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**\_Carimbo de data/hora D3DQUERYTYPE**
</dt> <dd>

Retorna um carimbo de data/hora de 64 bits.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE \_ TIMESTAMPDISJOINT**
</dt> <dd>

Use essa consulta para notificar um aplicativo se a frequência do contador tiver mudado do \_ carimbo de data/hora D3DQUERYTYPE.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE \_ TIMESTAMPFREQ**
</dt> <dd>

Esse resultado da consulta será **true** se os valores de \_ consultas de carimbo de data/hora D3DQUERYTYPE não puderem ser contínuos durante a \_ consulta D3DQUERYTYPE TIMESTAMPDISJOINT. Caso contrário, o resultado da consulta será **false**.

</dd> <dt>

<span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE \_ PIPELINETIMINGS**
</dt> <dd>

Porcentagem de tempo de processamento de dados do pipeline.

</dd> <dt>

<span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE \_ INTERFACETIMINGS**
</dt> <dd>

Porcentagem de tempo de processamento de dados no driver.

</dd> <dt>

<span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE \_ VERTEXTIMINGS**
</dt> <dd>

Porcentagem de tempo processando dados do sombreador de vértice.

</dd> <dt>

<span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE \_ PIXELTIMINGS**
</dt> <dd>

Porcentagem de tempo processando dados do sombreador de pixel.

</dd> <dt>

<span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE \_ BANDWIDTHTIMINGS**
</dt> <dd>

Comparações de medição de produtividade para ajudar na compreensão do desempenho de um aplicativo.

</dd> <dt>

<span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE \_ CACHEUTILIZATION**
</dt> <dd>

Meça o desempenho da taxa de acesso ao cache para texturas e vértices indexados.

</dd> <dt>

<span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE \_ MEMORYPRESSURE**
</dt> <dd>

Eficiência da alocação de memória contida em uma estrutura [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .

Diferenças entre o Direct3D 9 e o Direct3D 9Ex:

- o D3DQUERYTYPE \_ MEMORYPRESSURE só está disponível no Direct3D9Ex em execução no Windows 7 (ou mais no sistema operacional atual).



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9:: CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
