---
description: Obtém as interfaces de extensão que podem vir com um driver de dispositivo de aquisição de imagem do Windows (WIA) 2,0.
ms.assetid: 70f20f33-905c-4a88-8065-1cf876e98302
title: 'Método IWiaItem2:: GetExtension (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2fea4c4b9a2dd909b7ec49097ee94664b47f7e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010519"
---
# <a name="iwiaitem2getextension-method"></a>Método IWiaItem2:: GetExtension

Obtém as interfaces de extensão que podem vir com um driver de dispositivo de aquisição de imagem do Windows (WIA) 2,0.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] VOID   **ppOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Atualmente não utilizado. Deve ser definido como zero.

</dd> <dt>

*bstrname* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica o nome da extensão à qual o aplicativo de chamada requer um ponteiro.

<dt>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**


</dt> <dd>

A extensão do filtro de segmentação. Atualmente, esse é o único valor válido para esse parâmetro.

</dd> </dl> </dd> <dt>

*riidExtensionInterface* \[ no\]
</dt> <dd>

Tipo: **REFIID**

Especifica o identificador da interface de extensão.

</dd> <dt>

*ppOut* \[ fora\]
</dt> <dd>

Tipo: **void \* \***

Recebe o endereço de um ponteiro para a interface de extensão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Um aplicativo invoca esse método para criar um objeto de extensão que implementa uma das interfaces de extensão de driver WIA 2,0. **IWiaItem2:: GetExtension** armazena o endereço da interface de extensão do objeto de extensão no parâmetro *riidExtensionInterface* . Em seguida, o aplicativo usa o ponteiro de interface para chamar seus métodos.

Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *riidExtensionInterface* .

## <a name="examples"></a>Exemplos

CreateSegmentationFilter cria uma instância do [**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)(filtro de segmentação do driver) chamando **IWiaItem2:: GetExtension** na interface de [**IWiaItem2**](-wia-iwiaitem2.md) passada.


```C++
HRESULT
CreateSegmentationFilter(
   IWiaItem2               *pWiaItem2,
   IWiaSegmentationFilter  **ppSegmentationFilter)
{
   HRESULT                 hr         = S_OK;
   IWiaSegmentationFilter *pSegFilter = NULL;
    
   if (!pWiaItem2 || !ppSegmentationFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_SEGMENTATION_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->GetExtension(0,
                                      bstrFilterString,
                                      IID_IWiaSegmentationFilter,
                                      (void**)&pSegFilter);
         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   if (SUCCEEDED(hr))
   {
     *ppSegmentationFilter = pSegFilter;
      pSegFilter = NULL;
   }
   return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
