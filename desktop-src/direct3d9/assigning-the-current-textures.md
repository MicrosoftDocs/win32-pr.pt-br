---
description: O Direct3D mantém uma lista de até oito texturas atuais. Ele mistura essas texturas em todos os primitivos que renderiza. Somente as texturas criadas como ponteiros de interface de textura podem ser usadas no conjunto de texturas atuais.
ms.assetid: 5a58c915-7b67-45a7-9493-6657c75aaa10
title: Atribuindo as texturas atuais (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7ae6d603d9547841628f9395889095533cf3e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457190"
---
# <a name="assigning-the-current-textures-direct3d-9"></a>Atribuindo as texturas atuais (Direct3D 9)

O Direct3D mantém uma lista de até oito texturas atuais. Ele mistura essas texturas em todos os primitivos que renderiza. Somente as texturas criadas como ponteiros de interface de textura podem ser usadas no conjunto de texturas atuais.

Os aplicativos chamam o método [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) para atribuir texturas ao conjunto de texturas atuais. O primeiro parâmetro deve ser um número no intervalo de 0-7, inclusive. Passe o ponteiro da interface de textura como o segundo parâmetro.

O exemplo de código C++ a seguir demonstra como uma textura pode ser atribuída ao conjunto de texturas atuais.


```
// This code example assumes that the variable lpd3dDev is a
// valid pointer to an IDirect3DDevice9 interface and pTexture
// is a valid pointer to an IDirect3DBaseTexture9 interface.

// Set the third texture.
d3dDevice->SetTexture(2, pTexture);
```



> [!Note]  
> Os dispositivos de software não dão suporte à atribuição de uma textura a mais de um estágio de textura por vez.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mesclagem de textura](texture-blending.md)
</dt> </dl>

 

 
