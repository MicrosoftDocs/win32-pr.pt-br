---
description: Descreve como usar os métodos comuns das interfaces de coleção.
ms.assetid: 6ea311c0-a155-47de-ad40-62b0cbeb6e8f
title: Trabalhando com interfaces de coleção de OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cda84243347680d91a6f3a5255f7ebf4e66932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170118"
---
# <a name="working-with-xps-om-collection-interfaces"></a>Trabalhando com interfaces de coleção de OM XPS

Descreve como usar os métodos comuns das interfaces de coleção.

## <a name="contents"></a>Sumário

Os métodos descritos nesta seção são mostrados na lista a seguir. Nem todas as interfaces de coleção oferecem suporte a cada um desses métodos, e algumas interfaces também oferecem suporte a métodos que não estão descritos nesta página. Para obter a lista de métodos com suporte por uma interface específica, consulte a descrição da descrição dessa interface.

<dl>

[Método Append](#append-method)  
[Método GetAt](#getat-method)  
[Método GetCount](#getcount-method)  
[Método InsertAt](#insertat-method)  
[Método RemoveAt](#removeat-method)  
[Método SetAt](#setat-method)  
</dl>

[Consulte também](#see-also)

## <a name="append-method"></a>Método Append

Anexa um objeto ao final da coleção.

**Sintaxe genérica**


```C++
HRESULT Append(
  [in]  Object *object
);
```



**Descrição**

Para o final da coleção, esse método acrescenta um objeto que é passado na lista de parâmetros, conforme mostrado no diagrama a seguir.

![uma figura que mostra como Append adiciona uma entrada à coleção](images/generic-append.png)

## <a name="getat-method"></a>Método GetAt

Obtém um objeto de um local especificado na coleção.

**Sintaxe genérica**


```C++
HRESULT GetAt(
  [in]           UINT32 index,
  [out, retval]  Object **object
);
```



**Descrição**

Grava o objeto que é armazenado no local da coleção especificado pelo *índice* para a variável referenciada por *Object*. Essa ação não altera o conteúdo da coleção. O diagrama a seguir ilustra esse processo.

![uma figura que mostra como o GetAt recupera uma entrada da coleção](images/generic-getat.png)

## <a name="getcount-method"></a>Método GetCount

Obtém o número de objetos armazenados na coleção.

**Sintaxe genérica**


```C++
HRESULT GetCount(
  [out, retval]  UINT32 *count
);
```



**Descrição**

Grava o número de objetos que estão atualmente armazenados na coleção na variável referenciada por *Count*. Essa ação não altera o conteúdo da coleção. O diagrama a seguir ilustra esse processo.

![uma figura que mostra como GetCount Obtém o número de entradas na coleção](images/generic-getcount.png)

## <a name="insertat-method"></a>Método InsertAt

Insere um objeto em um local especificado da coleção.

**Sintaxe genérica**


```C++
HRESULT InsertAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



**Descrição**

O objeto passado no *objeto* é inserido na coleção no local especificado pelo *índice*. Antes de inserir o novo *objeto*, esse método move-se por 1 o objeto que ocupava anteriormente o local no *índice* e move todos os ponteiros de interface subsequentemente para *índice*. O diagrama a seguir ilustra esse processo.

![uma figura que mostra como o InsertAt adiciona uma entrada à coleção](images/generic-insertat.png)

## <a name="removeat-method"></a>Método RemoveAt

Remove o objeto de um local especificado na coleção.

**Sintaxe genérica**


```C++
HRESULT RemoveAt(
  [in]  UINT32 index
);
```



**Descrição**

Esse método libera o objeto do local especificado pelo *índice* e, em seguida, compacta a coleção reduzindo por 1 o índice de cada ponteiro subsequentemente para *indexar*. O diagrama a seguir ilustra esse processo.

![uma figura que mostra como RemoveAt remove uma entrada da coleção](images/generic-removeat.png)

## <a name="setat-method"></a>Método SetAt

Substitui o objeto em um local especificado na coleção.

**Sintaxe genérica**


```C++
HRESULT SetAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



**Descrição**

Esse método primeiro libera o objeto no local referenciado pelo *índice* e, em seguida, substitui esse objeto pelo que é passado no *objeto*. O diagrama a seguir ilustra esse processo.

![uma figura que mostra como SetAt substitui uma entrada na coleção](images/generic-setat.png)

## <a name="see-also"></a>Consulte Também

<dl>

[**IXpsOMColorProfileResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresourcecollection)  
[**IXpsOMDashCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)  
[**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)  
[**IXpsOMFontResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)  
[**IXpsOMGeometryFigureCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)  
[**IXpsOMGradientStopCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection)  
[**IXpsOMImageResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)  
[**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)  
[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)  
[**IXpsOMPartUriCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)  
[**IXpsOMRemoteDictionaryResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)  
[**IXpsOMSignatureBlockResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection)  
[**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)  
[**IXpsSignatureBlockCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)  
[**IXpsSignatureCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)  
[**IXpsSignatureRequestCollection**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)  
</dl>

 

 



