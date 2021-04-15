---
description: Define a classe de memória que mantém os buffers de um recurso.
ms.assetid: 29720b5f-16d7-4bd9-a7bd-e4dbfb00070b
title: Enumeração D3DPOOL (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPOOL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dc1d69d094b2f810855f9ce2116c472ba8ab605e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105747256"
---
# <a name="d3dpool-enumeration"></a>Enumeração D3DPOOL

Define a classe de memória que mantém os buffers de um recurso.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DPOOL { 
  D3DPOOL_DEFAULT      = 0,
  D3DPOOL_MANAGED      = 1,
  D3DPOOL_SYSTEMMEM    = 2,
  D3DPOOL_SCRATCH      = 3,
  D3DPOOL_FORCE_DWORD  = 0x7fffffff
} D3DPOOL, *LPD3DPOOL;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**D3DPOOL \_ padrão**
</dt> <dd>

Os recursos são colocados no pool de memória mais apropriado para o conjunto de usos solicitados para o recurso fornecido. Normalmente, essa é a memória de vídeo, incluindo a memória de vídeo local e a memória AGP. O \_ pool padrão D3DPOOL é separado de D3DPOOL \_ gerenciados e D3DPOOL \_ SYSTEMMEM e especifica que o recurso é colocado na memória preferencial para acesso ao dispositivo. Observe que D3DPOOL \_ Default nunca indica que D3DPOOL \_ gerenciado ou D3DPOOL \_ SYSTEMMEM devem ser escolhidos como o tipo de pool de memória para esse recurso. As texturas colocadas no \_ pool padrão D3DPOOL não podem ser bloqueadas a menos que sejam texturas dinâmicas ou sejam formatos de driver privados, FOURCC. Para acessar texturas inbloqueadas, você deve usar funções como [**IDirect3DDevice9:: UpdateSurface**](/windows/desktop/api), [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture), [**IDirect3DDevice9:: GetFrontBufferData**](/windows/desktop/api)e [**IDirect3DDevice9:: GetRenderTargetData**](/windows/desktop/api). \_O D3DPOOL gerenciado provavelmente é uma opção melhor do que o \_ padrão D3DPOOL para a maioria dos aplicativos. Observe que algumas texturas criadas nos formatos de pixel proprietários do driver, desconhecidos para o tempo de execução do Direct3D, podem ser bloqueadas. Observe também que-ao contrário de texturas – buffers de fundo de cadeia de troca, destinos de renderização, buffers de vértice e buffers de índice podem ser bloqueados. Quando um dispositivo é perdido, os recursos criados usando D3DPOOL \_ padrão devem ser liberados antes de chamar [**IDirect3DDevice9:: Reset**](/windows/desktop/api). Para obter mais informações, consulte [dispositivos perdidos (Direct3D 9)](lost-devices.md).

Ao criar recursos com D3DPOOL \_ padrão, se a memória da placa de vídeo já estiver confirmada, os recursos gerenciados serão removidos para liberar memória suficiente para atender à solicitação.

</dd> <dt>

<span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**\_Gerenciado D3DPOOL**
</dt> <dd>

Os recursos são copiados automaticamente para a memória acessível pelo dispositivo, conforme necessário. Os recursos gerenciados são apoiados pela memória do sistema e não precisam ser recriados quando um dispositivo é perdido. Consulte [Gerenciando recursos (Direct3D 9)](managing-resources.md) para obter mais informações. Os recursos gerenciados podem ser bloqueados. Somente a cópia da memória do sistema é modificada diretamente. O Direct3D copia suas alterações para a memória acessível por Driver, conforme necessário.



|                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferenças entre o Direct3D 9 e o Direct3D 9Ex:<br/> D3DPOOL \_ gerenciado é válido com [**IDirect3DDevice9**](/windows/desktop/api); no entanto, ele não é válido com [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex).<br/> |



 

</dd> <dt>

<span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**D3DPOOL \_ SYSTEMMEM**
</dt> <dd>

Os recursos são colocados na memória que normalmente não é acessível pelo dispositivo Direct3D. Essa alocação de memória consome RAM do sistema, mas não reduz a RAM paginável. Esses recursos não precisam ser recriados quando um dispositivo é perdido. Os recursos neste pool podem ser bloqueados e podem ser usados como a origem de uma operação [**IDirect3DDevice9:: UpdateSurface**](/windows/desktop/api) ou [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) para um recurso de memória criado com D3DPOOL \_ padrão.

</dd> <dt>

<span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**D3DPOOL \_ rascunho**
</dt> <dd>

Os recursos são colocados na RAM do sistema e não precisam ser recriados quando um dispositivo é perdido. Esses recursos não são associados por restrições de formato ou tamanho do dispositivo. Por isso, esses recursos não podem ser acessados pelo dispositivo Direct3D nem definidos como texturas ou destinos de renderização. No entanto, esses recursos sempre podem ser criados, bloqueados e copiados.

</dd> <dt>

<span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Todos os tipos de pool são válidos com todos os recursos, incluindo: buffers de vértice, buffers de índice, texturas e superfícies.

As tabelas a seguir indicam restrições em tipos de pool para destinos de renderização, estênceis de profundidade e usos dinâmico e mipmap. Um x indica uma combinação compatível; a falta de um x indica incompatibilidade.



| pool               | D3DUSAGE \_ RENDERTARGET | D3DUSAGE \_ DEPTHSTENCIL |
|--------------------|------------------------|------------------------|
| D3DPOOL \_ padrão   | x                      | x                      |
| \_Gerenciado D3DPOOL   |                        |                        |
| D3DPOOL \_ rascunho   |                        |                        |
| D3DPOOL \_ SYSTEMMEM |                        |                        |



 



| pool               | D3DUSAGE \_ dinâmico | D3DUSAGE \_ AUTOGENMIPMAP |
|--------------------|-------------------|-------------------------|
| D3DPOOL \_ padrão   | x                 | x                       |
| \_Gerenciado D3DPOOL   |                   | x                       |
| D3DPOOL \_ rascunho   |                   |                         |
| D3DPOOL \_ SYSTEMMEM | x                 |                         |



 

Para obter mais informações sobre tipos de uso, consulte [**D3DUSAGE**](d3dusage.md).

Os pools não podem ser misturados para objetos diferentes contidos em um recurso (níveis de MIP em um mipmap) e, quando um pool é escolhido, ele não pode ser alterado.

Os aplicativos devem usar \_ o D3DPOOL gerenciado para a maioria dos recursos estáticos, pois isso evita que o aplicativo tenha que lidar com dispositivos perdidos. (Os recursos gerenciados são restaurados pelo tempo de execução.) Isso é especialmente benéfico para sistemas de uma (arquitetura de memória unificada). Outros recursos dinâmicos não são uma boa correspondência para D3DPOOL \_ gerenciados. Na verdade, os buffers de índice e os buffers de vértice não podem ser criados usando D3DPOOL \_ gerenciados junto com o D3DUSAGE \_ Dynamic.

Para texturas dinâmicas, às vezes é desejável usar um par de texturas de memória de vídeo e de memória do sistema, alocando a memória de vídeo usando D3DPOOL \_ padrão e a memória do sistema usando o D3DPOOL \_ SYSTEMMEM. Você pode bloquear e modificar os bits da textura de memória do sistema usando um método de bloqueio. Em seguida, você pode atualizar a textura da memória de vídeo usando [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DUSAGE**](d3dusage.md)
</dt> <dt>

[**IDirect3DDevice9::CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
</dt> <dt>

[**IDirect3DDevice9::CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
</dt> <dt>

[**IDirect3DDevice9:: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
</dt> <dt>

[**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
</dt> <dt>

[**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
</dt> <dt>

[**D3DINDEXBUFFER \_ desc**](d3dindexbuffer-desc.md)
</dt> <dt>

[**D3DSURFACE \_ desc**](d3dsurface-desc.md)
</dt> <dt>

[**D3DVERTEXBUFFER \_ desc**](d3dvertexbuffer-desc.md)
</dt> <dt>

[**D3DVOLUME \_ desc**](d3dvolume-desc.md)
</dt> </dl>

 

 
