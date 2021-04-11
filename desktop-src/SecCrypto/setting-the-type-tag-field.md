---
description: Variáveis de tipo VARIANT têm um campo de marca de tipo VT que indica o tipo de dados dos dados.
ms.assetid: 3436faf6-2e66-46a1-b1e8-84f513282c16
title: Configurando o campo de marca de tipo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e443fae33b14bd4270e63188ff96a042a91c8e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164248"
---
# <a name="setting-the-type-tag-field"></a>Configurando o campo de marca de tipo

Variáveis de tipo **Variant** têm um campo de marca de tipo **VT** que indica o tipo de dados dos dados. Valores de retorno de tipo de **variante** são retornados por métodos com o campo de marca de tipo definido como o tipo de dados do valor de retorno. Os parâmetros de entrada do tipo **Variant** em uma chamada de método devem ter o campo de marca de tipo definido pelo aplicativo como um dos valores com suporte. A correspondência de tipos de parâmetro para tipos de dados é a seguinte.



| Tipo de parâmetro              | Tipo de dados                                      |
|-----------------------------|------------------------------------------------|
| PROPtype \_ longo<br/>   | VT \_ i2 ou VT \_ i4<br/>                    |
| data do PROPtype \_<br/>   | Data de VT \_<br/>                            |
| binário PROPtype \_<br/> | VT \_ BSTR ou (VT \_ BSTR \| VT \_ ByRef)<br/> |
| Cadeia de \_ caracteres proptype<br/> | VT \_ BSTR ou (VT \_ BSTR \| VT \_ ByRef)<br/> |



 

O exemplo a seguir mostra como inicializar os tipos de dados Variant listados acima.


```C++
HRESULT hr;
VARIANT vEMail;
VARIANT vNotBefore;
VARIANT vCount;
VARIANT vByRef;
BSTR bstr = NULL;
SYSTEMTIME st;

//Set the BSTR variant data type.
VariantInit(&vEMail);
vEMail.vt = VT_BSTR;   
vEMail.bstrVal = SysAllocString(L"someone@example.com");
if (NULL == vEMail.bstrVal)
{
    hr = E_OUTOFMEMORY;
    //Handle error.   
}
//Use the variant.
VariantClear(&vEMail);  //when done


//Set the BSTR|BYREF variant data type.
VariantInit(&vByRef);
vByRef.vt = VT_BSTR | VT_BYREF;   
vByRef.pbstrVal = &bstr;
//Use the variant.
VariantClear(&vByRef);  //when done
SysFreeString(bstr);


//Set the DATE variant data type.
memset(&st, 0, sizeof(SYSTEMTIME));
st.wYear = 2000;
st.wMonth = 1;
st.wDay = 1;
st.wHour = 12;

VariantInit(&vNotBefore);
vNotBefore.vt = VT_DATE;
if (!SystemTimeToVariantTime(&st, &vNotBefore.date))
{
    hr = E_FAIL;
    //Handle error.
}
//Use the variant.
VariantClear(&vNotBefore);  //when done


//Set the LONG variant data type.
VariantInit(&vCount);
vCount.vt = VT_I4;
vCount.long = 123456;
//Use the variant.
VariantClear(&vCount);  //when done
```



 

 




