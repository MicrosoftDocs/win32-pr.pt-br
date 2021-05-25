---
description: Uma combinação de zero ou mais opções de bloqueio que descrevem o tipo de bloqueio a ser executar.
ms.assetid: 46a611bd-a1ec-4967-b68d-72661d1b5cad
title: D3DLOCK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e4fcf8db9e60a30aee060dcc483b8d01e59b1c
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343191"
---
# <a name="d3dlock"></a>D3DLOCK

Uma combinação de zero ou mais opções de bloqueio que descrevem o tipo de bloqueio a ser executar.



| \#Definir                   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DLOCK \_ DISCARD           | O aplicativo descarta toda a memória dentro da região bloqueada. Para buffers de vértice e índice, todo o buffer será descartado. Essa opção só é válida quando o recurso é criado com uso dinâmico (consulte [D3DUSAGE](d3dusage.md)).                                                                                                                                                                                                                                                                                                                                                           |
| D3DLOCK \_ DONOTWAIT         | Permite que um aplicativo obtenha ciclos de CPU novamente se o driver não puder bloquear a superfície imediatamente. Se esse sinalizador for definido e o driver não puder bloquear a superfície imediatamente, a chamada de bloqueio retornará D3DERR \_ WASSTILLDRAWING. Esse sinalizador só pode ser usado ao bloquear uma superfície criada usando [**CreateOffscreenPlainSurface,**](/windows/desktop/api) [**CreateRenderTarget**](/windows/desktop/api)ou [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface). Esse sinalizador também pode ser usado com um buffer de fundo.            |
| D3DLOCK \_ SEM \_ ATUALIZAÇÃO \_ SUJA | Por padrão, um bloqueio em um recurso adiciona uma região suja a esse recurso. Essa opção impede qualquer alteração no estado sujo do recurso. Os aplicativos devem usar essa opção quando eles têm informações adicionais sobre o conjunto de regiões alteradas durante a operação de bloqueio.                                                                                                                                                                                                                                                                                                                    |
| D3DLOCK \_ NOOVERWRITE       | Indica que a memória referenciada em uma chamada de desenho desde o último bloqueio sem esse sinalizador não será modificada durante o bloqueio. Isso pode habilitar otimizações quando o aplicativo está acrescentando dados a um recurso. A especificação desse sinalizador permite que o driver retorne imediatamente se o recurso estiver em uso, caso contrário, o driver deverá terminar de usar o recurso antes de retornar do bloqueio.                                                                                                                                                                                            |
| D3DLOCK \_ NOSYSLOCK         | O comportamento padrão de um bloqueio de memória de vídeo é reservar uma seção crítica em todo o sistema, garantindo que nenhuma alteração no modo de exibição ocorrerá durante o bloqueio. Essa opção faz com que a seção crítica em todo o sistema não seja mantida durante o bloqueio.<br/> A operação de bloqueio é demorada, mas pode permitir que o sistema execute outras tarefas, como mover o cursor do mouse. Essa opção é útil para bloqueios de longa duração, como o bloqueio do buffer de fundo para a renderização de software que, de outra forma, afetaria negativamente a capacidade de resposta do sistema.<br/> |
| D3DLOCK \_ ReadOnly          | O aplicativo não gravará no buffer. Isso permite que os recursos armazenados em formatos não nativos salvem a etapa de recompactação ao desbloquear.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="constant-information"></a>Informações constantes



|  Requisito                        | Valor            |
|--------------------------|-------------|
| parâmetro                   | d3d9types. h |
| Sistema operacional mínimo | Windows 98  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes do Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**Proprietário**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**Proprietário**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[**Mínima**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**Cofre**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**LockIndexBuffer**](id3dxbasemesh--lockindexbuffer.md)
</dt> <dt>

[**LockVertexBuffer**](id3dxbasemesh--lockvertexbuffer.md)
</dt> <dt>

**LockVertexBuffer**
</dt> <dt>

[**LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

[**LockAttributeBuffer**](id3dxpatchmesh--lockattributebuffer.md)
</dt> <dt>

[**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md)
</dt> <dt>

[**LockVertexBuffer**](id3dxpatchmesh--lockvertexbuffer.md)
</dt> </dl>

 

 
