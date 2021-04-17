---
description: A estrutura PROPERTYINST define uma instância de uma propriedade em uma parte dos dados reconhecidos. Monitor de Rede aloca e preenche uma estrutura PROPERTYINST quando uma propriedade é anexada à captura.
ms.assetid: d8382a38-b634-4c65-b56b-44fee067a0fe
title: Estrutura PROPERTYINST (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINST
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5ee4ba108b8231646a2c0749dee6b5cc9f0f21c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755581"
---
# <a name="propertyinst-structure"></a><span data-ttu-id="5646c-104">Estrutura PROPERTYINST</span><span class="sxs-lookup"><span data-stu-id="5646c-104">PROPERTYINST structure</span></span>

<span data-ttu-id="5646c-105">A estrutura **PROPERTYINST** define uma instância de uma propriedade em uma parte dos dados reconhecidos.</span><span class="sxs-lookup"><span data-stu-id="5646c-105">The **PROPERTYINST** structure defines an instance of a property in a piece of recognized data.</span></span> <span data-ttu-id="5646c-106">Monitor de Rede aloca e preenche uma estrutura **PROPERTYINST** quando uma propriedade é anexada à captura.</span><span class="sxs-lookup"><span data-stu-id="5646c-106">Network Monitor allocates and fills in a **PROPERTYINST** structure when a property is attached to the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="5646c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5646c-107">Syntax</span></span>


```C++
typedef struct _PROPERTYINST {
  LPPROPERTYINFO lpPropertyInfo;
  LPSTR          szPropertyText;
  union {
    LPVOID           lpData;
    ULPBYTE          lpByte;
    ULPWORD          lpWord;
    ULPDWORD         lpDword;
    ULPLARGEINT      lpLargeInt;
    ULPSYSTEMTIME    lpSysTime;
    LPPROPERTYINSTEX lpPropertyInstEx;
  };
  WORD           DataLength;
  WORD           Level  :4;
  WORD           HelpID  :12;
  DWORD          IFlags;
} PROPERTYINST, *LPPROPERTYINST;
```



## <a name="members"></a><span data-ttu-id="5646c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5646c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5646c-109">**lpPropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="5646c-109">**lpPropertyInfo**</span></span>
</dt> <dd>

<span data-ttu-id="5646c-110">Ponteiro para a estrutura [PROPERTYINFO](propertyinfo.md) que define a propriedade.</span><span class="sxs-lookup"><span data-stu-id="5646c-110">Pointer to the [PROPERTYINFO](propertyinfo.md) structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="5646c-111">**szPropertyText**</span><span class="sxs-lookup"><span data-stu-id="5646c-111">**szPropertyText**</span></span>
</dt> <dd>

<span data-ttu-id="5646c-112">Ponteiro para uma cadeia de caracteres que é exibida no painel de detalhes da interface do usuário do Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="5646c-112">Pointer to a string that is displayed in the details pane of the Network Monitor UI.</span></span>

</dd> <dt>

<span data-ttu-id="5646c-113">**lpData**</span><span class="sxs-lookup"><span data-stu-id="5646c-113">**lpData**</span></span>
</dt> <dd>

<span data-ttu-id="5646c-114">Ponteiro para o início dos dados da propriedade.</span><span class="sxs-lookup"><span data-stu-id="5646c-114">Pointer to the start of the data for the property.</span></span> <span data-ttu-id="5646c-115">O analisador determina onde os dados de propriedade são iniciados.</span><span class="sxs-lookup"><span data-stu-id="5646c-115">The parser determines where the property data starts.</span></span>

</dd> <dt>

<span data-ttu-id="5646c-116">**lpByte**</span><span class="sxs-lookup"><span data-stu-id="5646c-116">**lpByte**</span></span>
</dt> <dd>

<span data-ttu-id="5646c-117">Ponteiro para os dados de **byte** .</span><span class="sxs-lookup"><span data-stu-id="5646c-117">Pointer to the **BYTE** data.</span></span>

</dd> <dt>

<span data-ttu-id="5646c-118">**lpWord**</span><span class="sxs-lookup"><span data-stu-id="5646c-118">**lpWord**</span></span>
</dt> <dd>

<span data-ttu-id="5646c-119">Ponteiro para os dados do **Word** .</span><span class="sxs-lookup"><span data-stu-id="5646c-119">Pointer to the **WORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="5646c-120">**lpDword**</span><span class="sxs-lookup"><span data-stu-id="5646c-120">**lpDword**</span></span>
</dt> <dd>

<span data-ttu-id="5646c-121">Ponteiro para os dados **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="5646c-121">Pointer to the **DWORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="5646c-122">**lpLargeInt**</span><span class="sxs-lookup"><span data-stu-id="5646c-122">**lpLargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="5646c-123">Ponteiro para os dados de [**LARGEINT**](largeint.md) .</span><span class="sxs-lookup"><span data-stu-id="5646c-123">Pointer to the [**LARGEINT**](largeint.md) data.</span></span>

</dd> <dt>

<span data-ttu-id="5646c-124">**lpSysTime**</span><span class="sxs-lookup"><span data-stu-id="5646c-124">**lpSysTime**</span></span>
</dt> <dd>

<span data-ttu-id="5646c-125">Ponteiro para os dados de [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="5646c-125">Pointer to the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) data.</span></span>

</dd> <dt>

<span data-ttu-id="5646c-126">**lpPropertyInstEx**</span><span class="sxs-lookup"><span data-stu-id="5646c-126">**lpPropertyInstEx**</span></span>
</dt> <dd>

<span data-ttu-id="5646c-127">Ponteiro para uma estrutura [PROPERTYINSTEX](propertyinstex.md) .</span><span class="sxs-lookup"><span data-stu-id="5646c-127">Pointer to a [PROPERTYINSTEX](propertyinstex.md) structure.</span></span> <span data-ttu-id="5646c-128">O membro **lpPropertyInstEx** é usado somente quando você chama [AttachPropertyInstanceEx](attachpropertyinstanceex.md).</span><span class="sxs-lookup"><span data-stu-id="5646c-128">The **lpPropertyInstEx** member is used only when you call [AttachPropertyInstanceEx](attachpropertyinstanceex.md).</span></span>

<span data-ttu-id="5646c-129">Se **lpPropertyInstEx** for usado, você deverá definir o membro **DATALENGTH** como 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="5646c-129">If **lpPropertyInstEx** is used, you must set the **DataLength** member to 0xFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="5646c-130">**DataLength**</span><span class="sxs-lookup"><span data-stu-id="5646c-130">**DataLength**</span></span>
</dt> <dd>

<span data-ttu-id="5646c-131">Comprimento dos dados desta instância da propriedade.</span><span class="sxs-lookup"><span data-stu-id="5646c-131">Data length for this instance of the property.</span></span> <span data-ttu-id="5646c-132">Se o membro **lpPropertyInstEx** apontar para uma estrutura [**PROPERTYINSTEX**](propertyinstex.md) , você deverá definir o **comprimento** de dados como 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="5646c-132">If the **lpPropertyInstEx** member points to a [**PROPERTYINSTEX**](propertyinstex.md) structure, you must set **DataLength** to 0xFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="5646c-133">**Level**</span><span class="sxs-lookup"><span data-stu-id="5646c-133">**Level**</span></span>
</dt> <dd>

<span data-ttu-id="5646c-134">Informações de nível.</span><span class="sxs-lookup"><span data-stu-id="5646c-134">Level information.</span></span>

</dd> <dt>

<span data-ttu-id="5646c-135">**HelpID**</span><span class="sxs-lookup"><span data-stu-id="5646c-135">**HelpID**</span></span>
</dt> <dd>

<span data-ttu-id="5646c-136">Identificador de contexto do arquivo de ajuda.</span><span class="sxs-lookup"><span data-stu-id="5646c-136">Help file context identifier.</span></span>

</dd> <dt>

<span data-ttu-id="5646c-137">**IFlags**</span><span class="sxs-lookup"><span data-stu-id="5646c-137">**IFlags**</span></span>
</dt> <dd>

<span data-ttu-id="5646c-138">Sinalizador de condição de erro.</span><span class="sxs-lookup"><span data-stu-id="5646c-138">Error condition flag.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5646c-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="5646c-139">Remarks</span></span>

<span data-ttu-id="5646c-140">A estrutura **PROPERTYINST** define uma instância de uma propriedade anexada.</span><span class="sxs-lookup"><span data-stu-id="5646c-140">The **PROPERTYINST** structure defines an instance of an attached property.</span></span> <span data-ttu-id="5646c-141">O analisador acessa a estrutura **PROPERTYINST** por meio de várias funções auxiliares.</span><span class="sxs-lookup"><span data-stu-id="5646c-141">The parser accesses the **PROPERTYINST** structure through several helper functions.</span></span> <span data-ttu-id="5646c-142">Por exemplo, quando a função [**FormatPropertyInstance**](formatpropertyinstance.md) é chamada para formatar os dados de uma propriedade, ela modifica o membro **SzPropertyText** da estrutura **PROPERTYINST** .</span><span class="sxs-lookup"><span data-stu-id="5646c-142">For example, when the [**FormatPropertyInstance**](formatpropertyinstance.md) function is called to format the data of a property, it modifies the **szPropertyText** member of the **PROPERTYINST** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5646c-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5646c-143">Requirements</span></span>



| <span data-ttu-id="5646c-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="5646c-144">Requirement</span></span> | <span data-ttu-id="5646c-145">Valor</span><span class="sxs-lookup"><span data-stu-id="5646c-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5646c-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5646c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="5646c-147">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5646c-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5646c-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5646c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="5646c-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5646c-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5646c-150">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5646c-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="5646c-151"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5646c-151"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5646c-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="5646c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5646c-153">AttachPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="5646c-153">AttachPropertyInstance</span></span>](attachpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="5646c-154">AttachPropertyInstanceEx</span><span class="sxs-lookup"><span data-stu-id="5646c-154">AttachPropertyInstanceEx</span></span>](attachpropertyinstanceex.md)
</dt> </dl>

 

