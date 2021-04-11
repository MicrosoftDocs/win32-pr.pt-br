---
description: O método doconfigure deve ser implementado pelo monitor. O MCSVC chama esse método para obter informações de configuração para a captura.
ms.assetid: bc2a3246-28dc-4452-a98e-a8a2447bb127
title: 'IMonitor: método oConfigure de:D (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoConfigure
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: e9a0ba2ade1095f291d5cb325a0902e6caeac3f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090254"
---
# <a name="imonitordoconfigure-method"></a><span data-ttu-id="656a7-104">IMonitor: método oConfigure de:D</span><span class="sxs-lookup"><span data-stu-id="656a7-104">IMonitor::DoConfigure method</span></span>

<span data-ttu-id="656a7-105">O método **doconfigure** deve ser implementado pelo monitor.</span><span class="sxs-lookup"><span data-stu-id="656a7-105">The **DoConfigure** method must be implemented by the monitor.</span></span> <span data-ttu-id="656a7-106">O MCSVC chama esse método para obter informações de configuração para a captura.</span><span class="sxs-lookup"><span data-stu-id="656a7-106">The MCSVC calls this method to obtain configuration information for the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="656a7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="656a7-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE DoConfigure(
  [in]  char *pName,
  [in]  char *pConfiguration,
  [out] char **ppScriptInstance
);
```



## <a name="parameters"></a><span data-ttu-id="656a7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="656a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="656a7-109">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="656a7-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656a7-110">Nome de uma instância do monitor.</span><span class="sxs-lookup"><span data-stu-id="656a7-110">Name of an instance of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="656a7-111">*pConfiguration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="656a7-111">*pConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656a7-112">Cadeia de caracteres de configuração fornecida pelo MCSVC.</span><span class="sxs-lookup"><span data-stu-id="656a7-112">Configuration string provided by the MCSVC.</span></span> <span data-ttu-id="656a7-113">O monitor deve analisar esta cadeia de caracteres para dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="656a7-113">The monitor must parse this string for configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="656a7-114">*ppScriptInstance* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="656a7-114">*ppScriptInstance* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="656a7-115">Endereço da cadeia de caracteres HTML usada para configurar o monitor.</span><span class="sxs-lookup"><span data-stu-id="656a7-115">Address of the HTML string used to configure the monitor.</span></span> <span data-ttu-id="656a7-116">Se um script padrão for usado para configuração, esse valor deverá ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="656a7-116">If a default script is used for configuration, this value should be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="656a7-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="656a7-117">Return value</span></span>

<span data-ttu-id="656a7-118">Se o método for bem-sucedido, o valor de retorno será S \_ OK (que é o mesmo que NOERROR) e o MCSVC executará o monitor.</span><span class="sxs-lookup"><span data-stu-id="656a7-118">If the method is successful, the return value is S\_OK (which is the same as NOERROR), and the MCSVC will run the monitor.</span></span>

<span data-ttu-id="656a7-119">Se o método não for bem-sucedido, o valor de retorno será um código de erro.</span><span class="sxs-lookup"><span data-stu-id="656a7-119">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="656a7-120">Um valor de retorno da \_ configuração do monitor NMERR \_ \_ é aceitável, mas quando esse erro é retornado, o monitor não pode iniciar até que uma chamada de **doconfigure** futura tenha êxito.</span><span class="sxs-lookup"><span data-stu-id="656a7-120">A return value of NMERR\_MONITOR\_CONFIG\_FAILED is acceptable, but when this error is returned, the monitor cannot start until a future **DoConfigure** call succeeds.</span></span> <span data-ttu-id="656a7-121">Qualquer outro erro impede que a instância do monitor seja habilitada.</span><span class="sxs-lookup"><span data-stu-id="656a7-121">Any other error prevents the instance of the monitor from being enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="656a7-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="656a7-122">Remarks</span></span>

<span data-ttu-id="656a7-123">O MCSVC chama esse método depois que ele se conectou à rede e antes do método [IRTC:: Configure](irtc-configure.md) ser chamado.</span><span class="sxs-lookup"><span data-stu-id="656a7-123">The MCSVC calls this method after it has connected to the network and before the [IRTC::Configure](irtc-configure.md) method is called.</span></span>

<span data-ttu-id="656a7-124">O monitor pode armazenar informações fornecidas por essa chamada, atualizar o script HTML ou a cadeia de caracteres de configuração e definir o [filtro de captura](capture-filters.md) no blob NPP.</span><span class="sxs-lookup"><span data-stu-id="656a7-124">The monitor can store information provided by this call, update the HTML script or configuration string, and set the [capture filter](capture-filters.md) in the NPP BLOB.</span></span>

<span data-ttu-id="656a7-125">O MCSVC pode chamar esse método várias vezes, mas não pode ser chamado enquanto o monitor estiver capturando dados.</span><span class="sxs-lookup"><span data-stu-id="656a7-125">The MCSVC may call this method several times, but it cannot be not called while the monitor is capturing data.</span></span> <span data-ttu-id="656a7-126">Observe que sempre que um [NPP](network-packet-providers.md) inicia uma captura, a conexão com a rede deve ser configurada.</span><span class="sxs-lookup"><span data-stu-id="656a7-126">Note that every time an [NPP](network-packet-providers.md) starts a capture, the connection to the network must be configured.</span></span> <span data-ttu-id="656a7-127">Essa restrição inclui situações em que o NPP é iniciado e interrompe a mesma captura.</span><span class="sxs-lookup"><span data-stu-id="656a7-127">This restriction includes situations in which the NPP starts and stops the same capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="656a7-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="656a7-128">Requirements</span></span>



| <span data-ttu-id="656a7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="656a7-129">Requirement</span></span> | <span data-ttu-id="656a7-130">Valor</span><span class="sxs-lookup"><span data-stu-id="656a7-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="656a7-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="656a7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="656a7-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="656a7-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="656a7-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="656a7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="656a7-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="656a7-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="656a7-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="656a7-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="656a7-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="656a7-136"><dt>Netmon.h</dt></span></span> </dl> |



 

 




