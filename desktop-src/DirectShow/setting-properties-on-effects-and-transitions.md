---
description: Definindo propriedades em efeitos e transições
ms.assetid: ce773140-7e50-4b72-8cb5-e34cba51644d
title: Definindo propriedades em efeitos e transições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1305eb7860b5519b14cfeebc349643c2662db3f133c0bf3424d1d71ccf85753c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904256"
---
# <a name="setting-properties-on-effects-and-transitions"></a>Definindo propriedades em efeitos e transições

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

muitos efeitos de [serviços de edição DirectShow](directshow-editing-services.md) e transições dão suporte a propriedades que controlam seu comportamento. Um aplicativo pode definir o valor de uma propriedade usando a interface [**IPropertySetter**](ipropertysetter.md) . O objeto de transição ou efeito subjacente deve dar suporte a **IDispatch** para definir as propriedades. Com efeitos de vídeo e transições, o aplicativo pode definir um intervalo de valores que mudam ao longo do tempo. (Por exemplo, você pode definir uma transição de apagamento para mover para frente e para trás pelo quadro.) Com efeitos de áudio, o valor da propriedade é estático e não pode ser alterado ao longo do tempo. A única exceção é o efeito de [envelope de volume](volume-envelope-effect.md) , que dá suporte a uma propriedade dinâmica para o nível de volume.

Para definir uma propriedade, execute as etapas a seguir.

1.  Crie uma instância do setter de propriedade (CLSID \_ PropertySetter).
2.  Preencha as estruturas [**Dexter \_ param**](dexter-param.md) e [**Dexter \_ Value**](dexter-value.md) com os dados de propriedade. Essas estruturas são discutidas abaixo.
3.  Passe as estruturas [**Dexter \_ param**](dexter-param.md) e [**Dexter \_ Value**](dexter-value.md) para o método [**IPropertySetter:: addprop**](ipropertysetter-addprop.md) .
4.  Repita as etapas 2 e 3 para cada propriedade que você deseja definir.
5.  Passe o ponteiro de interface [**IPropertySetter**](ipropertysetter.md) para o método [**IAMTimelineObj:: SetPropertySetter**](iamtimelineobj-setpropertysetter.md) .

A estrutura do [**\_ parâmetro Dexter**](dexter-param.md) especifica qual propriedade está sendo definida. Ele contém os membros a seguir.

-   **Nome**: o nome da propriedade
-   **DISPID**: reservado, deve ser zero
-   **nValores**: número de valores

A \_ estrutura de valor Dexter especifica o valor de uma propriedade em um determinado momento. Ele contém os membros a seguir.

-   **v**: tipo Variant que especifica um novo valor para a propriedade. O membro **VT** dessa variante define o tipo de dados da propriedade. para obter mais informações sobre o tipo **VARIANT** , consulte a SDK do Windows.
-   **RT**: tempo de referência quando a propriedade assume esse valor, em relação à hora de início do efeito ou da transição. A hora de início do efeito ou da transição é relativa à hora de início de seu objeto pai.
-   **dwInterp**: sinalizador que especifica como a propriedade é alterada do valor anterior para o novo valor. Com o \_ sinalizador de salto DEXTERF, a propriedade salta instantaneamente para o novo valor na hora especificada. Com o \_ sinalizador interpolação DEXTERF, a propriedade é interpolada linearmente do valor anterior.

Se você definir o membro **VT** como VT \_ BSTR, o setter da propriedade fará as conversões necessárias. Para valores de ponto flutuante, inclua o zero à esquerda antes da casa decimal. Por exemplo, 0,3, não. 3.

> [!Note]  
> Os aplicativos devem evitar depender da conversão de s **BSTR** para valores numéricos. Se a propriedade tiver um valor numérico, use o tipo numérico **Variant** apropriado é possível.

 

O valor de uma propriedade pode ser alterado com o passar do tempo, portanto, o método [**IPropertySetter:: addprop**](ipropertysetter-addprop.md) usa uma única estrutura de [**\_ parâmetro Dexter**](dexter-param.md) e um ponteiro para uma matriz de estruturas de [**\_ valor Dexter**](dexter-value.md) . A matriz define um conjunto de valores baseados em tempo para a propriedade. Os membros da matriz devem estar em ordem crescente de tempo e o membro **nValores** da \_ estrutura param Dexter deve ser igual ao comprimento da matriz.

O exemplo de código a seguir cria dados de propriedade para a transição de [apagamento SMPTE](smpte-wipe-transition.md) . Ele define o código de apagamento como 120, que cria um apagamento oval. Ele define o tempo de referência como zero, indicando o início da transição.


```C++
IPropertySetter     *pProp;   // Property setter
IAMTimelineObj      *pTransObj;  // Transition object
// Create an SMPTE Wipe transition object. (Not shown)

hr = CoCreateInstance(CLSID_PropertySetter, NULL, CLSCTX_INPROC_SERVER,
    IID_IPropertySetter, (void**) &pProp);

// Error checking is omitted for clarity...

DEXTER_PARAM param;
DEXTER_VALUE *pValue = (DEXTER_VALUE*)CoTaskMemAlloc(sizeof(DEXTER_VALUE));

// Initialize the parameter. 
param.Name = SysAllocString(L"MaskNum");
param.dispID = 0;
param.nValues = 1;

// Initialize the value.
pValue->v.vt = VT_I4;
pValue->v.lVal = 120; // Oval
pValue->rt = 0;
pValue->dwInterp = DEXTERF_JUMP;

pProp->AddProp(param, pValue);

// Free allocated resources.
SysFreeString(param.Name);
VariantClear(&(pValue->v));
CoTaskMemFree(pValue);

// Set the property on the transition.
pTransObj->SetPropertySetter(pProp);
pProp->Release();
```



**Alterando dinamicamente as propriedades**

Depois de renderizar um projeto de edição de vídeo, é possível modificar as propriedades de um efeito ou de um objeto de transição enquanto o grafo está em execução. No entanto, isso só será possível se você definir propriedades nesse objeto antes do aplicativo chamado [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md). Nesse caso, você pode chamar [**IAMTimelineObj:: GetPropertySetter**](iamtimelineobj-getpropertysetter.md) sobre o efeito ou a transição, limpar ou modificar as propriedades, e as alterações ocorrerão dinamicamente à medida que o grafo estiver em execução. Pode haver anomalias visuais enquanto a alteração ocorre, portanto, isso é recomendado apenas para visualização. Não altere as propriedades enquanto estiver gravando o projeto em um arquivo.

Se você não definiu nenhuma propriedade no objeto de efeito ou de transição antes de chamar **ConnectFrontEnd**, não será possível adicionar propriedades a ele enquanto o grafo estiver em execução.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com efeitos e transições](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



