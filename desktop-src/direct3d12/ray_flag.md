---
description: Sinalizadores passados para a função TraceRay para substituir transparência, remoção e comportamento de início.
ms.assetid: ''
title: Enumeração de RAY_FLAG
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 31d6a002e5f3f4eeb5f86e671be0904d61cb916d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762981"
---
# <a name="ray_flag-enumeration"></a>Enumeração de sinalizador de RAY \_

Sinalizadores passados para a função [**TraceRay**](traceray-function.md) para substituir transparência, remoção e comportamento de início.

## <a name="syntax"></a>Sintaxe


```
enum RAY_FLAG : uint
{
    RAY_FLAG_NONE                            = 0x00,
    RAY_FLAG_FORCE_OPAQUE                    = 0x01,
    RAY_FLAG_FORCE_NON_OPAQUE                = 0x02,
    RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH = 0x04,
    RAY_FLAG_SKIP_CLOSEST_HIT_SHADER         = 0x08,
    RAY_FLAG_CULL_BACK_FACING_TRIANGLES      = 0x10,
    RAY_FLAG_CULL_FRONT_FACING_TRIANGLES     = 0x20,
    RAY_FLAG_CULL_OPAQUE                     = 0x40,
    RAY_FLAG_CULL_NON_OPAQUE                 = 0x80,
}; 
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="RAY_FLAG_NONE"></span><span id="ray_flag_none"></span>**sinalizador de RAY \_ \_ None**
</dt> <dd>

Nenhuma opção selecionada.

</dd> <dt>

<span id="RAY_FLAG_FORCE_OPAQUE"></span><span id="ray_flag_force_opaque"></span>**sinalizador de RAY \_ \_ Force \_ opaco**
</dt> <dd>

Todas as interseções de Ray-Primitive encontradas em um raytrace são tratadas como opacas.  Portanto, nenhum sombreador de ocorrência será executado, independentemente de a geometria de ocorrência ou não especificar o \_ sinalizador de geometria D3D12 RAYTRACING \_ \_ \_ opaco e, independentemente dos sinalizadores de instância na instância que foi atingido.

Esse sinalizador é mutuamente exclusivo com o sinalizador de RAY \_ \_ Force \_ não \_ opaco, Ray \_ flag de \_ seleção \_ opaca e Ray \_ Flag \_ \_ não \_ opaco.


</dd> <dt>

<span id="RAY_FLAG_FORCE_NON_OPAQUE"></span><span id="ray_flag_force_non_opaque"></span>**sinalizador de RAY \_ \_ Force \_ não \_ opaco**
</dt> <dd>

Todas as interseções de Ray-Primitive encontradas em um raytrace são tratadas como não opacas.  Portanto, qualquer sombreador de ocorrências, se presente, será executado, independentemente de a geometria de ocorrência especificar ou não o \_ sinalizador de geometria D3D12 RAYTRACING \_ \_ \_ opaco e, independentemente dos sinalizadores de instância na instância que foi atingido.
Esse sinalizador é mutuamente exclusivo com o sinalizador de RAY \_ \_ FORCE_ \OPAQUE, Ray \_ flag de \_ seleção \_ opaca e Ray \_ flag de \_ seleção \_ não \_ opaco.


</dd> <dt>

<span id="RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH"></span><span id="ray_flag_accept_first_hit_and_end_search"></span>**o \_ sinalizador \_ de Ray aceita \_ primeira \_ jogada \_ e \_ finalizar \_ pesquisa**
</dt> <dd>

A primeira interseção Ray-Primitive encontrada em um raytrace faz com que **AcceptHitAndEndSearch** seja chamado imediatamente após o sombreador de qualquer clique, incluindo se não houver nenhum sombreador de clique. 
 
A única exceção é quando o sombreador de ocorrências anterior chama **IgnoreHit**; nesse caso, o raio continua inalterado, de modo que o próximo clique se torna outro candidato a ser a primeira ocorrência.  Para que essa exceção seja aplicada, o sombreador de qualquer clique tem que ser realmente executado.  Portanto, se o sombreador any for ignorado porque o pressionamento é tratado como opaco (por exemplo, devido ao sinalizador de RAY \_ \_ Force \_ opaco ou D3D12 RAYTRACING do sinalizador de \_ geometria opaco \_ \_ \_ ou D3D12 \_ RAYTRACING \_ \_ de instância \_ opaco que está sendo definido), então **AcceptHitAndEndSearch** é chamado.

Se um sombreador de clique mais próximo estiver presente no primeiro acesso, ele será invocado, a menos que o \_ \_ sombreador de clique de raio \_ mais próximo \_ \_ também esteja presente.  O único clique que foi encontrado é considerado "mais próximo", mesmo que outras ocorrências em potencial que possam estar mais próximas do raio possam não ter sido visitadas.

Um uso típico para esse sinalizador é para sombras, em que apenas um único pressionamento precisa ser encontrado.


</dd> <dt>

<span id="RAY_FLAG_SKIP_CLOSEST_HIT_SHADER"></span><span id="ray_flag_skip_closest_hit_shader"></span>**\_ \_ \_ sombreador de fechamento de omissão de \_ sinal de \_ Ray**
</dt> <dd>

Mesmo que pelo menos um clique tenha sido confirmado e o grupo de acesso para a visita mais próxima contenha um sombreador de clique mais próximo, ignore a execução desse sombreador. 

</dd> <dt>

<span id="RAY_FLAG_CULL_BACK_FACING_TRIANGLES"></span><span id="ray_flag_cull_back_facing_triangles"></span>**triângulos voltados para a remoção do sinalizador de RAY \_ \_ \_ \_ \_**
</dt> <dd>

Permite a remoção de triângulos voltados. Consulte **\_ sinalizadores de \_ instância \_ do D3D12 RAYTRACING** para selecionar quais triângulos são voltados, por instância.

Em instâncias que especificam \_ \_ o sinalizador de instância D3D12 RAYTRACING \_ \_ \_ \_ , desabilite o sinalizador.

Em tipos de geometria diferentes dos \_ \_ triângulos de tipo de geometria D3D12 RAYTRACING \_ \_ , esse sinalizador não tem nenhum efeito.

Esse sinalizador é mutuamente exclusivo com \_ \_ \_ \_ triângulos frontais de seleção de sinalizador de raio \_ .


</dd> <dt>

<span id="RAY_FLAG_CULL_FRONT_FACING_TRIANGLES"></span><span id="ray_flag_cull_front_facing_trianglesag_none"></span>**triângulos de seleção de sinalizador de RAY \_ \_ \_ - \_ face \_**
</dt> <dd>

Permite a remoção de triângulos frontais. Consulte **\_ sinalizadores de \_ instância \_ do D3D12 RAYTRACING** para selecionar quais triângulos são voltados, por instância.

Em instâncias que especificam \_ \_ o sinalizador de instância D3D12 RAYTRACING \_ \_ \_ \_ , desabilite o sinalizador.

Em tipos de geometria diferentes dos \_ \_ triângulos de tipo de geometria D3D12 RAYTRACING \_ \_ , esse sinalizador não tem nenhum efeito.

Esse sinalizador é mutuamente exclusivo com \_ \_ \_ \_ \_ triângulos voltados para a seleção de sinalizador de raio.


</dd> <dt>

<span id="RAY_FLAG_CULL_OPAQUE"></span><span id="ray_flag_cull_opaque"></span>**sinalizador de raio de \_ \_ seleção \_ opaco**
</dt> <dd>

Escolhe todos os primitivos que são considerados opacos com base em seus sinalizadores de geometria e de instância.

Esse sinalizador é mutuamente exclusivo com RAY \_ Flag \_ Force \_ opaco, Ray \_ Flag \_ Force \_ não \_ opaco e Ray \_ Flag \_ \_ não \_ opaco.


</dd> <dt>

<span id="RAY_FLAG_CULL_NON_OPAQUE"></span><span id="ray_flag_cull_non_opaque"></span>**\_seleção de sinalizador Ray \_ \_ não \_ opaco**
</dt> <dd>

Escolhe todos os primitivos que são considerados não opacos com base em seus sinalizadores de geometria e de instância.

Esse sinalizador é mutuamente exclusivo com RAY \_ Flag \_ Force \_ opaco, Ray \_ Flag \_ Force \_ não \_ opaco e Ray flag de \_ \_ seleção \_ opaca.


</dd>

## <a name="requirements"></a>Requisitos



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




