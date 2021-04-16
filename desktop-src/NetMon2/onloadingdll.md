---
description: Carrega a DLL do monitor.
ms.assetid: 6de2750f-3f12-4c0a-af8d-3ebd227fa123
title: Função OnLoadingDLL (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnLoadingDLL
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b2d9d728065818b1e94fa436f4d1e9b62dbeb5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787045"
---
# <a name="onloadingdll-function"></a><span data-ttu-id="bdf1c-103">Função OnLoadingDLL</span><span class="sxs-lookup"><span data-stu-id="bdf1c-103">OnLoadingDLL function</span></span>

<span data-ttu-id="bdf1c-104">A função **OnLoadingDLL** carrega a DLL do monitor.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-104">The **OnLoadingDLL** function loads the monitor DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdf1c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bdf1c-105">Syntax</span></span>


```C++
HRESULT OnLoadingDLL(
  _Inout_ HBLOB hFilterBlob,
  _In_    DWORD *pCreateFlags,
  _Out_   char  **ppDefaultName,
  _Out_   char  **ppDescription,
  _Out_   char  **ppDefaultScript,
  _Out_   char  **ppDefaultConfig
);
```



## <a name="parameters"></a><span data-ttu-id="bdf1c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdf1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdf1c-107">*hFilterBlob* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="bdf1c-107">*hFilterBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf1c-108">Um BLOB que o MCSVC usa para corresponder a um monitor com NICs disponíveis.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-108">A BLOB that the MCSVC uses to match a monitor with available NICs.</span></span> <span data-ttu-id="bdf1c-109">Esse parâmetro sempre contém uma solicitação para uma interface [IRTC](irtc.md) , de modo que a maioria dos monitores não precisa adicionar nenhuma entrada ao blob.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-109">This parameter always contains a request for an [IRTC](irtc.md) interface, so most monitors do not need to add any entries to the BLOB.</span></span> <span data-ttu-id="bdf1c-110">No entanto, um monitor personalizado pode adicionar critérios de filtro adicionais (por exemplo, que o tipo de MAC deve ser Ethernet).</span><span class="sxs-lookup"><span data-stu-id="bdf1c-110">However, a custom monitor can add additional filter criteria (for example, that the MAC type must be Ethernet).</span></span>

</dd> <dt>

<span data-ttu-id="bdf1c-111">*pCreateFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bdf1c-111">*pCreateFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf1c-112">Os sinalizadores que indicam como o MCSVC controla a criação de um monitor.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-112">The flags that indicate how the MCSVC controls the creation of a monitor.</span></span> <span data-ttu-id="bdf1c-113">Esse parâmetro deve ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="bdf1c-113">This parameter must be one of the following values:</span></span>



| <span data-ttu-id="bdf1c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="bdf1c-114">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="bdf1c-115">Significado</span><span class="sxs-lookup"><span data-stu-id="bdf1c-115">Meaning</span></span>                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_CREATE_ONE_PER_NETCARD"></span><span id="mcs_create_one_per_netcard"></span><dl> <span data-ttu-id="bdf1c-116"><dt>**MCS \_ criar \_ um \_ por \_ Netcard**</dt></span><span class="sxs-lookup"><span data-stu-id="bdf1c-116"><dt>**MCS\_CREATE\_ONE\_PER\_NETCARD**</dt></span></span> </dl>          | <span data-ttu-id="bdf1c-117">O MCSVC garante que apenas uma instância desse monitor exista para cada NIC.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-117">The MCSVC ensures that only one instance of this monitor exists for each NIC.</span></span> <span data-ttu-id="bdf1c-118">Uma segunda instância só poderá ser criada se a primeira for destruída.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-118">A second instance can be created only if the first one is destroyed.</span></span><br/> |
| <span id="MCS_CREATE_CONFIGS_BY_DEFAULT"></span><span id="mcs_create_configs_by_default"></span><dl> <span data-ttu-id="bdf1c-119"><dt>**\_ \_ configurações de MCS Create \_ por \_ padrão**</dt></span><span class="sxs-lookup"><span data-stu-id="bdf1c-119"><dt>**MCS\_CREATE\_CONFIGS\_BY\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="bdf1c-120">Se o monitor tiver uma configuração interna padrão, o MCSVC não exigirá que o usuário configure o monitor antes que a instância seja criada.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-120">If the monitor has a default internal configuration, the MCSVC does not require the user to configure the monitor before the instance is created.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="bdf1c-121">*ppDefaultName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bdf1c-121">*ppDefaultName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf1c-122">Um ponteiro para um ponteiro para o endereço do nome padrão do monitor.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-122">A pointer to a pointer to the address of the default name of the monitor.</span></span> <span data-ttu-id="bdf1c-123">O MCSVC usa o nome padrão ao criar instâncias do monitor.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-123">The MCSVC uses the default name when creating instances of the monitor.</span></span>

<span data-ttu-id="bdf1c-124">Por exemplo, se o nome padrão retornado for "monitor do roteador", a primeira instância do monitor será "monitor do roteador 1", o segundo seria "RouterMonitor2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-124">For example, if the returned default name is "Router Monitor", the first monitor instance would be "Router Monitor 1", the second would be "RouterMonitor2, and so on.</span></span> <span data-ttu-id="bdf1c-125">Se **NULL** for retornado, o MCSVC usará o nome da dll.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-125">If **NULL** is returned, the MCSVC uses the name of the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="bdf1c-126">*ppDescription* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bdf1c-126">*ppDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf1c-127">Um ponteiro para um ponteiro para o endereço da descrição do monitor.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-127">A pointer to a pointer to the address of the description of the monitor.</span></span> <span data-ttu-id="bdf1c-128">A descrição é passada para a ferramenta de controle de monitor, que usa a descrição para indicar ao usuário que o monitor existe.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-128">The description is passed to the Monitor Control Tool, which uses the description to indicate to the user that the monitor exists.</span></span> <span data-ttu-id="bdf1c-129">Esse parâmetro pode retornar **NULL**.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-129">This parameter can return **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bdf1c-130">*ppDefaultScript* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bdf1c-130">*ppDefaultScript* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf1c-131">Um ponteiro para um ponteiro para o endereço do script de formulário HTML padrão usado para configurar o monitor.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-131">A pointer to a pointer to the address of the default HTML Form script used to configure the monitor.</span></span> <span data-ttu-id="bdf1c-132">Embora as instâncias do monitor possam alterar seu próprio script, a maioria dos monitores simplesmente carrega seu script uma vez, de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-132">Although the instances of the monitor can alter their own script, most monitors simply load their script once, from a file.</span></span> <span data-ttu-id="bdf1c-133">O valor de *ppDefaultScript* pode ser **nulo**; no entanto, o monitor não pode ser configurado externamente ou deve fornecer um script mais tarde.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-133">The value of *ppDefaultScript* can be **NULL**; however, then either the monitor cannot be externally configured, or it must supply a script later.</span></span> <span data-ttu-id="bdf1c-134">É mais eficiente fornecer um script padrão aqui.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-134">It is more efficient to supply a default script here.</span></span>

</dd> <dt>

<span data-ttu-id="bdf1c-135">*ppDefaultConfig* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bdf1c-135">*ppDefaultConfig* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf1c-136">O endereço da cadeia de caracteres padrão usada para configurar o monitor quando ele é criado.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-136">The address of the default string used to configure the monitor when it is created.</span></span> <span data-ttu-id="bdf1c-137">Esse parâmetro pode ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-137">This parameter can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdf1c-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bdf1c-138">Return value</span></span>

<span data-ttu-id="bdf1c-139">Se a função for bem-sucedida, o valor de retorno será S Ok, o \_ que é o mesmo que NOERROR.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-139">If the function is successful, the return value is S\_OK; which is the same as NOERROR.</span></span>

<span data-ttu-id="bdf1c-140">Se a função não for bem-sucedida, o MCSVC omitirá o monitor especificado de todas as suas listas; Depois, nenhum monitor desse tipo pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-140">If the function is unsuccessful, the MCSVC omits the specified monitor from all its lists; after, no monitor of this type can be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdf1c-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="bdf1c-141">Remarks</span></span>

<span data-ttu-id="bdf1c-142">A função **OnLoadingDLL** é chamada uma vez por MCSVC, quando carrega pela primeira vez a dll.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-142">The **OnLoadingDLL** function is called once by the MCSVC, when it first loads the DLL.</span></span> <span data-ttu-id="bdf1c-143">Em seguida, a DLL fornece os valores padrão que serão usados pelo MCSVC ao criar uma instância de um monitor.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-143">The DLL then provides the default values that will be used by the MCSVC when creating an instance of a monitor.</span></span>

<span data-ttu-id="bdf1c-144">O monitor deve alocar toda a memória necessária para as cadeias de caracteres retornadas para o MCSVC.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-144">The monitor must allocate all the necessary memory for the strings returned to the MCSVC.</span></span> <span data-ttu-id="bdf1c-145">No retorno, o MCSVC faz cópias de todas as cadeias de caracteres e não tentará liberar as cadeias de caracteres retornadas.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-145">On return, the MCSVC makes copies of all the strings and will not attempt to free the returned strings.</span></span>

<span data-ttu-id="bdf1c-146">O monitor deve usar funções auxiliares de BLOB para alterar o BLOB de filtro.</span><span class="sxs-lookup"><span data-stu-id="bdf1c-146">The monitor should use BLOB helper functions to alter the filter BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdf1c-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdf1c-147">Requirements</span></span>



| <span data-ttu-id="bdf1c-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdf1c-148">Requirement</span></span> | <span data-ttu-id="bdf1c-149">Valor</span><span class="sxs-lookup"><span data-stu-id="bdf1c-149">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bdf1c-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdf1c-150">Minimum supported client</span></span><br/> | <span data-ttu-id="bdf1c-151">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bdf1c-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bdf1c-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdf1c-152">Minimum supported server</span></span><br/> | <span data-ttu-id="bdf1c-153">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bdf1c-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bdf1c-154">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bdf1c-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdf1c-155"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdf1c-155"><dt>Netmon.h</dt></span></span> </dl> |



 

 




