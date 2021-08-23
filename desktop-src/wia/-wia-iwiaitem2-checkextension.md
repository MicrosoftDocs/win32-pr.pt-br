---
description: Verifica se uma extensão especificada está disponível no computador e pode ser usada pelo método IWiaItem2::GetExtension.
ms.assetid: 672f6418-4ce3-4570-a412-fe639c9f5eb8
title: Método IWiaItem2::CheckExtension (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CheckExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 50240fbf10155fae555c6cd2e30bf8c86c571b8d52b86e02eab9f5bb11ac17ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965575"
---
# <a name="iwiaitem2checkextension-method"></a>Método IWiaItem2::CheckExtension

Verifica se uma extensão especificada está disponível no computador e pode ser usada pelo método [**IWiaItem2::GetExtension.**](-wia-iwiaitem2-getextension.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] BOOL   *pbExtensionExists
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ Em\]
</dt> <dd>

Tipo: **LONG**

Atualmente não éusado. Deve ser definido como zero.

</dd> <dt>

*bstrName* \[ Em\]
</dt> <dd>

Tipo: **BSTR**

Especifica o nome da extensão.

</dd> <dt>

*riidExtensionInterface* \[ Em\]
</dt> <dd>

Tipo: **REFIID**

Atualmente não éusado.

</dd> <dt>

*pbExtensionExists* \[ out\]
</dt> <dd>

Tipo: **BOOL \***

Recebe um ponteiro para um **BOOL.**

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False**


</dt> <dd>

A extensão especificada não está disponível.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdade**


</dt> <dd>

A extensão especificada está disponível.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Usando esse método, os aplicativos podem verificar se uma extensão está disponível antes de chamar o [**método IWiaItem2::GetExtension.**](-wia-iwiaitem2-getextension.md) Além disso, o aplicativo pode verificar quais extensões estão disponíveis sem co-criar cada uma delas e, em seguida, decidir qual delas usar.

## <a name="examples"></a>Exemplos

CheckImgFilter verifica se o driver tem um filtro de processamento de imagem. Antes de chamar o componente de visualização, um aplicativo deve garantir que o driver tenha um filtro de processamento de imagem.


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   return hr;

}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




