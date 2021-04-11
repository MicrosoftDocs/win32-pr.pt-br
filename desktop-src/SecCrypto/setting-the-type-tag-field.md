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
# <a name="setting-the-type-tag-field"></a><span data-ttu-id="ba10a-103">Configurando o campo de marca de tipo</span><span class="sxs-lookup"><span data-stu-id="ba10a-103">Setting the Type Tag Field</span></span>

<span data-ttu-id="ba10a-104">Variáveis de tipo **Variant** têm um campo de marca de tipo **VT** que indica o tipo de dados dos dados.</span><span class="sxs-lookup"><span data-stu-id="ba10a-104">**VARIANT** type variables have a type tag field **vt** that indicates the data type of the data.</span></span> <span data-ttu-id="ba10a-105">Valores de retorno de tipo de **variante** são retornados por métodos com o campo de marca de tipo definido como o tipo de dados do valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="ba10a-105">**VARIANT** type return values are returned by methods with the type tag field set to the data type of the return value.</span></span> <span data-ttu-id="ba10a-106">Os parâmetros de entrada do tipo **Variant** em uma chamada de método devem ter o campo de marca de tipo definido pelo aplicativo como um dos valores com suporte.</span><span class="sxs-lookup"><span data-stu-id="ba10a-106">**VARIANT** type input parameters in a method call must have the type tag field set by the application to one of the supported values.</span></span> <span data-ttu-id="ba10a-107">A correspondência de tipos de parâmetro para tipos de dados é a seguinte.</span><span class="sxs-lookup"><span data-stu-id="ba10a-107">The correspondence of parameter types to data types is as follows.</span></span>



| <span data-ttu-id="ba10a-108">Tipo de parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba10a-108">Parameter type</span></span>              | <span data-ttu-id="ba10a-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ba10a-109">Data type</span></span>                                      |
|-----------------------------|------------------------------------------------|
| <span data-ttu-id="ba10a-110">PROPtype \_ longo</span><span class="sxs-lookup"><span data-stu-id="ba10a-110">PROPTYPE\_LONG</span></span><br/>   | <span data-ttu-id="ba10a-111">VT \_ i2 ou VT \_ i4</span><span class="sxs-lookup"><span data-stu-id="ba10a-111">VT\_I2 or VT\_I4</span></span><br/>                    |
| <span data-ttu-id="ba10a-112">data do PROPtype \_</span><span class="sxs-lookup"><span data-stu-id="ba10a-112">PROPTYPE\_DATE</span></span><br/>   | <span data-ttu-id="ba10a-113">Data de VT \_</span><span class="sxs-lookup"><span data-stu-id="ba10a-113">VT\_DATE</span></span><br/>                            |
| <span data-ttu-id="ba10a-114">binário PROPtype \_</span><span class="sxs-lookup"><span data-stu-id="ba10a-114">PROPTYPE\_BINARY</span></span><br/> | <span data-ttu-id="ba10a-115">VT \_ BSTR ou (VT \_ BSTR \| VT \_ ByRef)</span><span class="sxs-lookup"><span data-stu-id="ba10a-115">VT\_BSTR or (VT\_BSTR \| VT\_BYREF)</span></span><br/> |
| <span data-ttu-id="ba10a-116">Cadeia de \_ caracteres proptype</span><span class="sxs-lookup"><span data-stu-id="ba10a-116">PROPTYPE\_STRING</span></span><br/> | <span data-ttu-id="ba10a-117">VT \_ BSTR ou (VT \_ BSTR \| VT \_ ByRef)</span><span class="sxs-lookup"><span data-stu-id="ba10a-117">VT\_BSTR or (VT\_BSTR \| VT\_BYREF)</span></span><br/> |



 

<span data-ttu-id="ba10a-118">O exemplo a seguir mostra como inicializar os tipos de dados Variant listados acima.</span><span class="sxs-lookup"><span data-stu-id="ba10a-118">The following example shows how to initialize the variant data types listed above.</span></span>


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



 

 




