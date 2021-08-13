---
description: Os materiais descrevem como os polígonos refletem a luz ou parecem emitir luz em uma cena 3D.
ms.assetid: vs|directx_sdk|~\materials.htm
title: Materiais (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8140de30243c7a0f7290715da3d0720cd15cea769bd78cbf66893c0082062d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092940"
---
# <a name="materials-direct3d-9"></a>Materiais (Direct3D 9)

Os materiais descrevem como os polígonos refletem a luz ou parecem emitir luz em uma cena 3D. As propriedades de material detalham a reflexão difusa de um material, a reflexão de ambiente, a emissão de luz e as características de realce especular. O Direct3D usa a estrutura [**D3DMATERIAL9**](d3dmaterial9.md) para transportar todas as informações de propriedade de material. Com exceção da propriedade especular, cada propriedade é descrita como uma cor RGBA que representa a quantidade de partes vermelha, verde e azul de um determinado tipo de luz que ele reflete e um fator de mistura alfa.

## <a name="diffuse-and-ambient-reflection"></a>Difuso e reflexo de ambiente

Os membros difuso e de ambiente da estrutura [**D3DMATERIAL9**](d3dmaterial9.md) descrevem como um material reflete o ambiente e a luz difusa em uma cena. Como a maioria das cenas contém muito mais luz difusa do que a luz ambiente, a reflexão difusa desempenha a maior parte na determinação da cor. Além disso, como a luz difusa é direcional, o ângulo de incidência para a luz difusa afeta a intensidade geral da reflexão. A reflexão difusa é maior quando a luz atinge um vértice paralelo ao vértice normal. À medida que o ângulo aumenta, o efeito da reflexão difusa diminui. A quantidade de luz refletida é o cosseno do ângulo entre a luz de entrada e o vértice normal, conforme mostrado na ilustração a seguir.

![ilustração da quantidade de luz refletida](images/incident.png)

A reflexão de ambiente, como a luz ambiente, não é direcional. A reflexão de ambiente tem um impacto menor na cor aparente de um objeto renderizado, mas afeta a cor geral e é mais perceptível quando pouco ou nenhuma luz difusa reflete o material. A reflexão de ambiente de um material é afetada pela luz ambiente definida para uma cena chamando o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) com o \_ sinalizador de ambiente D3DRS.

A forma difusa e a reflexão de ambiente funcionam em conjunto para determinar a cor percebida de um objeto e geralmente são valores idênticos. Por exemplo, para renderizar um objeto Blue crystalline, você cria um material que reflete apenas o componente azul da luz difusa e ambiente. Quando colocado em uma sala com uma luz branca, o cristal parece azul. No entanto, em uma sala que tem apenas uma luz vermelha, o mesmo cristal pareceria preto, porque seu material não reflete a luz vermelha.

## <a name="emission"></a>Emissão

Os materiais podem ser usados para fazer com que um objeto renderizado pareça ser Luminous. O membro emissiva da estrutura [**D3DMATERIAL9**](d3dmaterial9.md) é usado para descrever a cor e a transparência da luz emitida. A emissão afeta a cor de um objeto e pode, por exemplo, tornar um material escuro mais claro e adotar parte da cor emitida.

Você pode usar a propriedade emissiva de um material para adicionar a ilusão de que um objeto está emitindo luz, sem incorrer na sobrecarga computacional de adicionar uma luz à cena. No caso do Crystal azul, a propriedade emissiva será útil se você quiser fazer com que o Crystal pareça acender, mas não convertê-la em outros objetos da cena. Lembre-se de que os materiais com as propriedades emissiva não emitem a luz que pode ser refletida por outros objetos em uma cena. Para atingir essa luz refletida, você precisa inserir uma luz adicional dentro da cena.

## <a name="specular-reflection"></a>Reflexão especular

A reflexão especular cria destaques em objetos, fazendo com que eles pareçam brilhantes. A estrutura [**D3DMATERIAL9**](d3dmaterial9.md) contém dois membros que descrevem a cor de realce especular, bem como a luminosidade geral do material. Você estabelece a cor dos destaques especulares Configurando o membro especular para a cor RGBA desejada-as cores mais comuns são brancas ou cinza claro. Os valores definidos no membro de energia controlam a nitidez dos efeitos especulares.

Os destaques especulares podem criar efeitos consideráveis. Desenhando novamente na analogia do cristal azul: um valor de potência maior cria destaques mais nítidos, fazendo com que o cristal pareça ser bastante brilhante. Valores menores aumentam a área do efeito, criando uma reflexão de graça que torna o cristal claro. Para tornar um objeto realmente fosco, defina o membro de energia como zero e a cor em especular como preto. Experimente diferentes níveis de reflexão para produzir uma aparência realista para suas necessidades. A ilustração a seguir mostra dois modelos idênticos. Aquele à esquerda usa uma potência de reflexo especular de 10; o modelo à direita não tem nenhuma reflexão especular.

![ilustração de modelos de reflexo especulares](images/spechigh.png)

## <a name="setting-material-properties"></a>Definindo propriedades de material

Dispositivos de renderização de Direct3D podem ser renderizados com um conjunto de propriedades de material por vez.

Em um aplicativo C++, você define as propriedades de material que o sistema usa ao preparar uma estrutura [**D3DMATERIAL9**](d3dmaterial9.md) e, em seguida, chamar o método [**IDirect3DDevice9:: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) .

Para preparar a estrutura [**D3DMATERIAL9**](d3dmaterial9.md) para uso, defina as informações de propriedade na estrutura para criar o efeito desejado durante a renderização. O exemplo de código a seguir configura a estrutura **D3DMATERIAL9** para um material roxo com destaques de especular branco nítido.


```
D3DMATERIAL9 mat;

// Set the RGBA for diffuse reflection.
mat.Diffuse.r = 0.5f;
mat.Diffuse.g = 0.0f;
mat.Diffuse.b = 0.5f;
mat.Diffuse.a = 1.0f;

// Set the RGBA for ambient reflection.
mat.Ambient.r = 0.5f;
mat.Ambient.g = 0.0f;
mat.Ambient.b = 0.5f;
mat.Ambient.a = 1.0f;

// Set the color and sharpness of specular highlights.
mat.Specular.r = 1.0f;
mat.Specular.g = 1.0f;
mat.Specular.b = 1.0f;
mat.Specular.a = 1.0f;
mat.Power = 50.0f;

// Set the RGBA for emissive color.
mat.Emissive.r = 0.0f;
mat.Emissive.g = 0.0f;
mat.Emissive.b = 0.0f;
mat.Emissive.a = 0.0f;
```



Depois de preparar a estrutura [**D3DMATERIAL9**](d3dmaterial9.md) , aplique as propriedades chamando o método [**IDirect3DDevice9:: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) do dispositivo de renderização. Esse método aceita o endereço de uma estrutura **D3DMATERIAL9** preparada como seu único parâmetro. Você pode chamar **IDirect3DDevice9:: SetMaterial** com novas informações conforme necessário para atualizar as propriedades de material para o dispositivo. O exemplo de código a seguir mostra como isso pode parecer com o código.


```
// This code example uses the material properties defined for 
// the mat variable earlier in this topic. The pd3dDev is assumed
// to be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
hr = pd3dDev->SetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



Quando você cria um dispositivo Direct3D, o material atual é definido automaticamente como o padrão mostrado na tabela a seguir.



| Membro   | Valor                |
|----------|----------------------|
| Difusa  | (R:0, G:0, B:0, A:0) |
| Especular | (R:0, G:0, B:0, A:0) |
| Ambiente  | (R:0, G:0, B:0, A:0) |
| Emissiva | (R:0, G:0, B:0, A:0) |
| Energia    | (0,0)                |



 

## <a name="retrieving-material-properties"></a>Recuperando propriedades de material

Você recupera as propriedades de material que o dispositivo de renderização está usando no momento chamando o método [**IDirect3DDevice9:: GetMaterial**](/windows/desktop/api) para o dispositivo. Ao contrário do método [**IDirect3DDevice9:: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) , o **IDirect3DDevice9:: GetMaterial** não requer preparação. O método **IDirect3DDevice9:: GetMaterial** aceita o endereço de uma estrutura [**D3DMATERIAL9**](d3dmaterial9.md) e preenche a estrutura fornecida com informações que descrevem as propriedades do material atual antes de retornar.


```
// For this example, the pd3dDev variable is assumed to 
// be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
D3DMATERIAL9 mat;

hr = pd3dDev->GetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



> [!Note]  
> Se o seu aplicativo não especificar as propriedades do material para renderização, o sistema usará um material padrão. O material padrão reflete todas as difusos-branco, por exemplo, sem reflexão de ambiente ou especulação e nenhuma cor de emissiva.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Luzes e materiais](lights-and-materials.md)
</dt> </dl>

 

 
