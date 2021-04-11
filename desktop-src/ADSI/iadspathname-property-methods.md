---
title: Métodos de propriedade IADsPathname (IADs. h)
description: Obter ou definir as propriedades de Escapemode.
ms.assetid: 007ec617-cff2-492a-a62c-50d65fefcd3b
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsPathname
topic_type:
- apiref
api_name:
- IADsPathname Property Methods
- IADsPathname.EscapedMode
- IADsPathname.get_EscapedMode
- IADsPathname.get_EscapedMode
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 949bd41ddb04618d238c0ddf09782e12fb228b26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163605"
---
# <a name="iadspathname-property-methods"></a><span data-ttu-id="c91a6-104">Métodos de propriedade IADsPathname</span><span class="sxs-lookup"><span data-stu-id="c91a6-104">IADsPathname Property Methods</span></span>

<span data-ttu-id="c91a6-105">Os métodos de propriedade da interface [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) obtêm ou definem as propriedades de **escapemode** .</span><span class="sxs-lookup"><span data-stu-id="c91a6-105">The property methods of the [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) interface get or set the **EscapedMode** properties.</span></span> <span data-ttu-id="c91a6-106">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="c91a6-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="c91a6-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c91a6-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="c91a6-108">**Escapemode**</span><span class="sxs-lookup"><span data-stu-id="c91a6-108">**EscapedMode**</span></span>
<span data-ttu-id="c91a6-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c91a6-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="c91a6-110">Examine ou especifique como os caracteres de escape são tratados em um nome de caminho.</span><span class="sxs-lookup"><span data-stu-id="c91a6-110">Examine or specify how escaped characters are handled in a pathname.</span></span> <span data-ttu-id="c91a6-111">Para obter mais informações e opções definidas, [**consulte \_ \_ \_ enumeração do modo de escape do ADS**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span><span class="sxs-lookup"><span data-stu-id="c91a6-111">For more information and defined options, see [**ADS\_ESCAPE\_MODE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span></span>

<dt>

<span data-ttu-id="c91a6-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c91a6-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c91a6-113">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="c91a6-113">Scripting data type: **Long**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EscapedMode(
  [out] long* retval
);
HRESULT get_EscapedMode(
  [in] long* lnEscapedMode
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="c91a6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c91a6-114">Remarks</span></span>

<span data-ttu-id="c91a6-115">**Escapemode** representa um estado.</span><span class="sxs-lookup"><span data-stu-id="c91a6-115">**EscapedMode** represents a state.</span></span> <span data-ttu-id="c91a6-116">Você pode ativá-la ou desligá-la, definindo-a como ADS \_ escapemode \_ on ou ADS outmode \_ /ADS escapemode \_ \_ \_ off \_ ex.</span><span class="sxs-lookup"><span data-stu-id="c91a6-116">You can turn it on or off, by setting it to ADS\_ESCAPEDMODE\_ON or ADS\_ESCAPEDMODE\_OFF/ADS\_ESCAPEDMODE\_OFF\_EX.</span></span> <span data-ttu-id="c91a6-117">Quando ativado ou desativado, todas as recuperações subsequentes produzem cadeias de caracteres de caminho de escape ou sem escape.</span><span class="sxs-lookup"><span data-stu-id="c91a6-117">When it is turned on, or off, all subsequent retrievals produce escaped or unescaped path strings.</span></span>

<span data-ttu-id="c91a6-118">No ADSI, somente o [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) é capaz de refazer a saída de caminhos.</span><span class="sxs-lookup"><span data-stu-id="c91a6-118">In ADSI only the [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) is capable of unescaping paths.</span></span> <span data-ttu-id="c91a6-119">Todas as outras interfaces ADSI sempre retornam caminhos com escape.</span><span class="sxs-lookup"><span data-stu-id="c91a6-119">All other ADSI interfaces always return escaped paths.</span></span> <span data-ttu-id="c91a6-120">O estado padrão de **escapemode** é ADS \_ de escapemode \_ padrão, conforme definido na [**enumeração do modo de escape do ADS \_ \_ \_**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span><span class="sxs-lookup"><span data-stu-id="c91a6-120">The default state of **EscapedMode** is ADS\_ESCAPEDMODE\_DEFAULT as defined in [**ADS\_ESCAPE\_MODE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span></span>

## <a name="examples"></a><span data-ttu-id="c91a6-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c91a6-121">Examples</span></span>

<span data-ttu-id="c91a6-122">O exemplo de código a seguir mostra como usar a propriedade **escapemode** ativar/desativar a saída dos três caracteres especiais a seguir: "=", "," e "/".</span><span class="sxs-lookup"><span data-stu-id="c91a6-122">The following code example shows how to use the **EscapedMode** property turn on/off escaping of the following three special characters: "=",",", and "/".</span></span>


```VB
Dim path As New Pathname
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All escaped, producing:
                                          ' "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' Only "/" is unescaped:
                                          ' "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
```



<span data-ttu-id="c91a6-123">O exemplo de código a seguir mostra como usar a propriedade **escapemode** ativar/desativar a saída dos três caracteres especiais a seguir: "=", "," e "/".</span><span class="sxs-lookup"><span data-stu-id="c91a6-123">The following code example shows how to use the **EscapedMode** property turn on/off escaping of the following three special characters: "=",",", and "/".</span></span>


```VB
<%
Dim path
const ADS_SETTYPE_FULL = 1
const ADS_SETTYPE_DN   = 4
const ADS_FORMAT_WINDOWS = 1
const ADS_ESCAPEDMODE_ON = 2
const ADS_ESCAPEDMODE_OFF = 3
const ADS_ESCAPEDMODE_OFF_EX = 4
 
Set path = CreateObject("Pathname")
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' All escaped, producing:  "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' Only "/" is unescaped: "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
%>
```



<span data-ttu-id="c91a6-124">O exemplo de código a seguir mostra como trabalhar com a propriedade **escapemode** .</span><span class="sxs-lookup"><span data-stu-id="c91a6-124">The following code example shows how to work with the **EscapedMode** property.</span></span> <span data-ttu-id="c91a6-125">A verificação de erros foi ignorada.</span><span class="sxs-lookup"><span data-stu-id="c91a6-125">Error checking is ignored.</span></span>


```C++
IADsPathname *pPathname=NULL;
HRESULT hr;
 
hr = CoCreateInstance(CLSID_Pathname,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsPathname,
                      (void**)&pPathname);
 
if(FAILED(hr)) 
{
    if(pPathname) pPathname->Release();
    return NULL;
}
 
pPathname->AddRef();
hr = pPathname->Set(CComBSTR("LDAP://CN=joy/ful\/*"), 
                    ADS_SETTYPE_FULL); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy/ful\/*"

SysFreeString(bstr);
 
// Set the path using ADS_SETTYPE_DN
 
hr = pPathname->Set(CComBSTR("CN=joy/ful\/*"), ADS_SETTYPE_DN); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy\/ful\/*"

SysFreeString(bstr);
 
hr = pPathname->Release();
```



## <a name="requirements"></a><span data-ttu-id="c91a6-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c91a6-126">Requirements</span></span>



| <span data-ttu-id="c91a6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c91a6-127">Requirement</span></span> | <span data-ttu-id="c91a6-128">Valor</span><span class="sxs-lookup"><span data-stu-id="c91a6-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c91a6-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c91a6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c91a6-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c91a6-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c91a6-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c91a6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c91a6-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c91a6-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c91a6-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c91a6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c91a6-134"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="c91a6-134"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="c91a6-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c91a6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c91a6-136"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c91a6-136"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="c91a6-137">IID</span><span class="sxs-lookup"><span data-stu-id="c91a6-137">IID</span></span><br/>                      | <span data-ttu-id="c91a6-138">IID \_ IADsPathname é definido como D592AED4-F420-11D0-A36E-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="c91a6-138">IID\_IADsPathname is defined as D592AED4-F420-11D0-A36E-00C04FB950DC</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="c91a6-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="c91a6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c91a6-140">**IADsPathname**</span><span class="sxs-lookup"><span data-stu-id="c91a6-140">**IADsPathname**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspathname)
</dt> <dt>

[<span data-ttu-id="c91a6-141">**\_enumeração do \_ modo de escape do ADS \_**</span><span class="sxs-lookup"><span data-stu-id="c91a6-141">**ADS\_ESCAPE\_MODE\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)
</dt> </dl>

 

 





