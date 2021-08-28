---
description: Opções para salvar e criar efeitos.
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6858f659b1561a526a284b3ea2dca0e1d9a11a31
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624082"
---
# <a name="d3dxfx"></a>D3DXFX

Opções para salvar e criar efeitos.

As constantes na tabela a seguir são definidas em d3dx9effect.h.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Sinalizadores de salvar e restaurar estado de efeito</td>
<td>Descrição</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESTATE</td>
<td>Nenhum estado é salvo ao chamar <a href="id3dxeffect--begin.md"><strong>Begin ou</strong></a> restaurado ao chamar <a href="id3dxeffect--end.md"><strong>End</strong></a>.</td>
</tr>
<tr class="odd">
<td>D3DXFX_DONOTSAVESAMPLERSTATE</td>
<td>Um stateblock salva o estado ao chamar <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> e restaura o estado ao chamar <a href="id3dxeffect--end.md"><strong>End</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESHADERSTATE</td>
<td>Um stateblock salva o estado (exceto sombreadores e constantes de sombreador) ao chamar <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> e restaura o estado ao chamar <a href="id3dxeffect--end.md"><strong>End</strong></a>.</td>
</tr>
<tr class="odd">
<td>Sinalizadores de criação de efeito</td>
<td>Descrição</td>
</tr>
<tr class="even">
<td>D3DXFX_NOT_CLONEABLE</td>
<td>O efeito será não clonável e não conterá nenhum dado binário do sombreador. <a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc não</strong></a> retornará ponteiros de função de sombreador. Definir esse sinalizador reduz o uso de memória de efeito em cerca de 50%, pois elimina a necessidade do sistema de efeito manter uma cópia dos sombreadores na memória. Esse sinalizador é usado por <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>e <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</td>
</tr>
<tr class="odd">
<td>D3DXFX_LARGEADDRESSAWARE</td>
<td>Habilita a alocação de um recurso de efeito no espaço de endereço uppder de um computador. Uma limitação importante é que você não pode usar cadeias de caracteres e lida de forma intercambiável. Por exemplo, o seguinte não funcionaria mais. <span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>g_pEffect->SetMatrix( &quot;g_mWorldViewProjection&quot;, &mWorldViewProjection );</code></pre></td>
</tr>
</tbody>
</table>

Em vez disso, um método como [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) deve ser usado para armazenar o handle do parâmetro , que é usado para passar variáveis para o efeito.</td>
</tr>
</tbody>
</table>



 

As constantes na tabela a seguir não são definidas por padrão e devem ser definidas pelo desenvolvedor.



| Pré-processador de efeito \# define | Descrição                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXFX \_ LARGEADDRESS \_ HANDLE   | Defina esse valor antes de incluir d3dx9.h para que seu aplicativo não seja compilado ao tentar passar cadeias de caracteres para parâmetros D3DXHANDLE. Isso auxiliará a garantir que as informações válidas estão sendo passadas para o runtime. |
| Sinalizadores do Vinculador de Efeito            | Descrição                                                                                                                                                                                                                          |
| GRANDE \_ CONHECIMENTO DE \_ ENDEREÇO          | Definir o sinalizador do vinculador LARGE ADDRESS AWARE = 1 permitirá que o aplicativo aloce recursos após o limite de \_ \_ endereços de 2 GB quando necessário.                                                                                      |



 

O sistema de efeito usa blocos de estado para salvar e restaurar o estado automaticamente. Para obter mais informações sobre blocos de estado, consulte Estado de salvar e restaurar [blocos de estado (Direct3D 9)](state-blocks-save-and-restore-state.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes de efeito](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



