---
description: Conjunto de propriedades de PIN
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: Conjunto de propriedades de PIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53955ba1f075094c4fb2f6324ed143ca54f72c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909613"
---
# <a name="pin-property-set"></a>Conjunto de propriedades de PIN

O conjunto de propriedades PIN retorna a categoria de PIN de um PIN em um filtro. A categoria é definida pelo filtro quando ele cria o PIN; a categoria indica que tipo de dados o PIN é entregue ou recebe por esse PIN.



| Label | Valor |
|-------------------|----------------------|
| GUID do Conjunto de Propriedades | **AMPROPSETID \_ PIN** |



 



| ID da propriedade                   | Descrição                      |
|-------------------------------|----------------------------------|
| **\_categoria AMPROPERTY PIN \_** | Especifica a categoria de um PIN. |



 

O DirectShow define as seguintes categorias de PIN no arquivo de cabeçalho UUIDs. h.



| GUID da categoria                     | Descrição                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FIXAR \_ categoria \_ ANALOGVIDEOIN**  | Pino de entrada do filtro de captura que usa analógico e digitalizado.                                                                                                                                                                                                                                                     |
| **FIXAR \_ captura de categoria \_**        | Capturar PIN.                                                                                                                                                                                                                                                                                                            |
| **FIXAR \_ categoria \_ CC**             | PIN fornecendo dados de legenda codificada da linha 21.                                                                                                                                                                                                                                                                      |
| **FIXAR \_ categoria \_ EDS**            | PIN fornecendo serviços de dados estendidos (linha 21, até mesmo campos).                                                                                                                                                                                                                                                            |
| **FIXAR \_ categoria \_ NABTS**          | PIN que fornece dados padrão do norte da América do Videotext.                                                                                                                                                                                                                                                                   |
| **FIXAR \_ Visualização da categoria \_**        | PIN de visualização.                                                                                                                                                                                                                                                                                                            |
| **FIXAR \_ categoria \_ ainda**          | PIN que fornece uma imagem ainda. O PIN de captura do filtro deve ser conectado antes que o PIN da imagem ainda esteja conectado.                                                                                                                                                                                                    |
| **FIXAR \_ o \_ teletexto da categoria**       | PIN fornecendo teletexto (uma variante de legenda oculta).                                                                                                                                                                                                                                                                   |
| **código de panela da categoria do PIN \_ \_**       | PIN fornecendo dados de código de code.                                                                                                                                                                                                                                                                                            |
| **FIXAR \_ categoria \_ VBI**            | PIN fornecendo dados de intervalo em branco vertical.                                                                                                                                                                                                                                                                          |
| **FIXAR \_ categoria \_ VIDEOPORT**      | Pino de saída de vídeo a ser conectado ao pino de entrada zero no [mixer de sobreposição](overlay-mixer-filter.md).                                                                                                                                                                                                                    |
| **FIXAR \_ categoria \_ VIDEOPORT \_ VBI** | PIN a ser conectado ao [alocador de superfície VBI](vbi-surface-allocator.md), o filtro de alocador de superfície VBI necessário para alocar a memória de vídeo correta para itens como sobreposições de legendagem oculta em cenários em que uma porta de vídeo está sendo usada. Cenários PCI, IEEE 1394 e USB não usam esse filtro. |
| **\_captura de vídeo \_ CC \_ do PINNAME**   | Fatia de hardware-pino de legenda fechado                                                                                                                                                                                                                                                                                  |



 

Esta propriedade é somente para leitura.

### <a name="example-code"></a>Código de exemplo

O código a seguir mostra como verificar se um PIN dá suporte a esse conjunto de propriedades e, nesse caso, como obter a categoria do PIN:


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



> [!Note]  
> Este exemplo usa a função [SafeRelease](../medfound/saferelease.md) para liberar ponteiros de interface.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Requisitos de PIN para filtros de captura](pin-requirements-for-capture-filters.md)
</dt> <dt>

[Conjuntos de propriedades](property-sets.md)
</dt> <dt>

[Trabalhando com categorias de PIN](working-with-pin-categories.md)
</dt> </dl>

 

 
