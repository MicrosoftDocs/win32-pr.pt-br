---
description: Opções para salvar e criar efeitos.
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9077c8c7e3da479dd8963484bc289b84093ac0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995073"
---
# <a name="d3dxfx"></a>D3DXFX

Opções para salvar e criar efeitos.

As constantes na tabela a seguir são definidas em d3dx9effect. h.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Sinalizadores de salvamento e restauração de estado do efeito</td>
<td>Descrição</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESTATE</td>
<td>Nenhum estado é salvo ao chamar <a href="id3dxeffect--begin.md"><strong>begin</strong></a> ou restaurado ao chamar <a href="id3dxeffect--end.md"><strong>end</strong></a>.</td>
</tr>
<tr class="odd">
<td>D3DXFX_DONOTSAVESAMPLERSTATE</td>
<td>Um stateblock salva o estado ao chamar <a href="id3dxeffect--begin.md"><strong>begin</strong></a> e restaura o estado ao chamar <a href="id3dxeffect--end.md"><strong>end</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESHADERSTATE</td>
<td>Um stateblock salva o estado (exceto sombreadores e constantes de sombreador) ao chamar <a href="id3dxeffect--begin.md"><strong>begin</strong></a> e restaura o estado ao chamar <a href="id3dxeffect--end.md"><strong>end</strong></a>.</td>
</tr>
<tr class="odd">
<td>Sinalizadores de criação de efeito</td>
<td>Descrição</td>
</tr>
<tr class="even">
<td>D3DXFX_NOT_CLONEABLE</td>
<td>O efeito será não clonável e não conterá dados binários de sombreador. <a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> não retornará ponteiros de função de sombreador. Definir esse sinalizador reduz o uso de memória de efeito em cerca de 50%, pois elimina a necessidade do sistema de efeito manter uma cópia dos sombreadores na memória. Esse sinalizador é usado por <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>e <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</td>
</tr>
<tr class="odd">
<td>D3DXFX_LARGEADDRESSAWARE</td>
<td>Habilita a alocação de um recurso de efeito no espaço de endereço uppder de um computador. Uma limitação importante é que você não pode usar cadeias de caracteres e identificadores de forma intercambiável. Por exemplo, o seguinte não funcionaria mais. <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>g_pEffect->SetMatrix( &quot;g_mWorldViewProjection&quot;, &mWorldViewProjection );</code></pre></td>
</tr>
</tbody>
</table>

Em vez disso, um método como [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) deve ser usado para armazenar o identificador do parâmetro, que é então usado para passar variáveis para o efeito.</td>
</tr>
</tbody>
</table>



 

As constantes na tabela a seguir não são definidas por padrão e devem ser definidas pelo desenvolvedor.



| Vigorar \# definição do pré-processador | Descrição                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXFX \_ LARGEADDRESS \_ Handle   | Defina esse valor antes de incluir d3dx9. h para que seu aplicativo não seja compilado ao tentar passar cadeias de caracteres para parâmetros D3DXHANDLE. Isso ajudará a garantir que as informações válidas sejam passadas para o tempo de execução. |
| Sinalizadores do vinculador de efeito            | Descrição                                                                                                                                                                                                                          |
| \_reconhecimento de endereço grande \_          | Definir o sinalizador do vinculador com \_ reconhecimento de endereço grande \_ = 1 permitirá que o aplicativo aloque recursos após o limite de endereços de 2GB, quando necessário.                                                                                      |



 

O sistema de efeitos usa blocos de estado para salvar e restaurar o estado automaticamente. Para obter mais informações sobre blocos de estado, consulte estado de [salvamento e restauração de blocos de estado (Direct3D 9)](state-blocks-save-and-restore-state.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes de efeito](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



