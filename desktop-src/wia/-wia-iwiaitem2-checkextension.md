---
description: 'Verifica se uma extensão especificada está disponível no computador e pode ser usada pelo método IWiaItem2:: GetExtension.'
ms.assetid: 672f6418-4ce3-4570-a412-fe639c9f5eb8
title: 'Método IWiaItem2:: CheckExtension (WIA. h)'
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
ms.openlocfilehash: 65b0b5b3ace1634a20dfa63382d82099fef0686e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761635"
---
# <a name="iwiaitem2checkextension-method"></a>Método IWiaItem2:: CheckExtension

Verifica se uma extensão especificada está disponível no computador e pode ser usada pelo método [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) .

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

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Atualmente não utilizado. Deve ser definido como zero.

</dd> <dt>

*bstrname* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica o nome da extensão.

</dd> <dt>

*riidExtensionInterface* \[ no\]
</dt> <dd>

Tipo: **REFIID**

Atualmente não utilizado.

</dd> <dt>

*pbExtensionExists* \[ fora\]
</dt> <dd>

Tipo: **bool \** _

Recebe um ponteiro para um _ * BOOL * *.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FOR**


</dt> <dd>

A extensão especificada não está disponível.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE**


</dt> <dd>

A extensão especificada está disponível.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Usando esse método, os aplicativos podem verificar se uma extensão está disponível antes de chamar o método [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) . Além disso, o aplicativo pode verificar quais extensões estão disponíveis sem a criação de cada uma delas e, em seguida, decidir qual delas usar.

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




