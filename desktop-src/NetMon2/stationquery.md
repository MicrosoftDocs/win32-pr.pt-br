---
description: A estrutura STATIONQUERY fornece informações sobre um computador específico usando Monitor de Rede.
ms.assetid: b7202c6b-e2b9-4a6f-8b87-3d11879f1d69
title: Estrutura STATIONQUERY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONQUERY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: de76c4da7bc27d76c04aeeaa7a46d69134e411ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758418"
---
# <a name="stationquery-structure"></a><span data-ttu-id="1ce08-103">Estrutura STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="1ce08-103">STATIONQUERY structure</span></span>

<span data-ttu-id="1ce08-104">A estrutura **STATIONQUERY** fornece informações sobre um computador específico usando monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="1ce08-104">The **STATIONQUERY** structure provides information about a specific computer using Network Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ce08-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ce08-105">Syntax</span></span>


```C++
typedef struct _STATIONQUERY {
  DWORD Flags;
  BYTE  BCDVerMinor;
  BYTE  BCDVerMajor;
  DWORD LicenseNumber;
  BYTE  MachineName[MACHINE_NAME_LENGTH];
  BYTE  UserName[USER_NAME_LENGTH];
  BYTE  Reserved[32];
  BYTE  AdapterAddress[6];
  WCHAR WMachineName[MACHINE_NAME_LENGTH];
  WCHAR WUserName[USER_NAME_LENGTH];
} STATIONQUERY, *LPSTATIONQUERY;
```



## <a name="members"></a><span data-ttu-id="1ce08-106">Membros</span><span class="sxs-lookup"><span data-stu-id="1ce08-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1ce08-107">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="1ce08-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="1ce08-108">Sinalizadores que identificam o estado atual de Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="1ce08-108">Flags that Identify the current state of Network Monitor.</span></span>



| <span data-ttu-id="1ce08-109">Valor</span><span class="sxs-lookup"><span data-stu-id="1ce08-109">Value</span></span>                                                                                                                                                                                                                | <span data-ttu-id="1ce08-110">Significado</span><span class="sxs-lookup"><span data-stu-id="1ce08-110">Meaning</span></span>                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="STATIONQUERY_FLAGS_LOADED"></span><span id="stationquery_flags_loaded"></span><dl> <span data-ttu-id="1ce08-111"><dt>**\_sinalizadores STATIONQUERY \_ carregados**</dt></span><span class="sxs-lookup"><span data-stu-id="1ce08-111"><dt>**STATIONQUERY\_FLAGS\_LOADED**</dt></span></span> </dl>                   | <span data-ttu-id="1ce08-112">O driver está carregado, mas o kernel não é.</span><span class="sxs-lookup"><span data-stu-id="1ce08-112">The driver is loaded, but the kernel is not.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_RUNNING"></span><span id="stationquery_flags_running"></span><dl> <span data-ttu-id="1ce08-113"><dt>**STATIONQUERY \_ sinalizadores \_ em execução**</dt></span><span class="sxs-lookup"><span data-stu-id="1ce08-113"><dt>**STATIONQUERY\_FLAGS\_RUNNING**</dt></span></span> </dl>                | <span data-ttu-id="1ce08-114">O driver está carregado, mas não está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="1ce08-114">The driver is loaded but not capturing data.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_CAPTURING"></span><span id="stationquery_flags_capturing"></span><dl> <span data-ttu-id="1ce08-115"><dt>**\_captura de sinalizadores STATIONQUERY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1ce08-115"><dt>**STATIONQUERY\_FLAGS\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="1ce08-116">O driver está ativamente envolvido em uma captura.</span><span class="sxs-lookup"><span data-stu-id="1ce08-116">The driver is actively engaged in a capture.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_TRANSMITTING"></span><span id="stationquery_flags_transmitting"></span><dl> <span data-ttu-id="1ce08-117"><dt>**STATIONQUERY \_ sinalizadores de \_ transmissão**</dt></span><span class="sxs-lookup"><span data-stu-id="1ce08-117"><dt>**STATIONQUERY\_FLAGS\_TRANSMITTING**</dt></span></span> </dl> | <span data-ttu-id="1ce08-118">Esse sinalizador é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="1ce08-118">This flag is obsolete.</span></span><br/>                       |



 

</dd> <dt>

<span data-ttu-id="1ce08-119">**BCDVerMinor**</span><span class="sxs-lookup"><span data-stu-id="1ce08-119">**BCDVerMinor**</span></span>
</dt> <dd>

<span data-ttu-id="1ce08-120">Número de versão secundária de Monitor de Rede instalado no computador.</span><span class="sxs-lookup"><span data-stu-id="1ce08-120">Minor version number of Network Monitor installed on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="1ce08-121">**BCDVerMajor**</span><span class="sxs-lookup"><span data-stu-id="1ce08-121">**BCDVerMajor**</span></span>
</dt> <dd>

<span data-ttu-id="1ce08-122">Número de versão principal do Monitor de Rede instalado no computador.</span><span class="sxs-lookup"><span data-stu-id="1ce08-122">Major version number of Network Monitor installed on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="1ce08-123">**LicenseNumber**</span><span class="sxs-lookup"><span data-stu-id="1ce08-123">**LicenseNumber**</span></span>
</dt> <dd>

<span data-ttu-id="1ce08-124">Número de licença do software.</span><span class="sxs-lookup"><span data-stu-id="1ce08-124">Software license number.</span></span>

</dd> <dt>

<span data-ttu-id="1ce08-125">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="1ce08-125">**MachineName**</span></span>
</dt> <dd>

<span data-ttu-id="1ce08-126">Nome do fabricante do computador, se houver.</span><span class="sxs-lookup"><span data-stu-id="1ce08-126">Computer manufacturer name, if any.</span></span>

</dd> <dt>

<span data-ttu-id="1ce08-127">**UserName**</span><span class="sxs-lookup"><span data-stu-id="1ce08-127">**UserName**</span></span>
</dt> <dd>

<span data-ttu-id="1ce08-128">Nome de usuário ou identificador do sistema.</span><span class="sxs-lookup"><span data-stu-id="1ce08-128">User name or system identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1ce08-129">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="1ce08-129">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="1ce08-130">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="1ce08-130">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="1ce08-131">**AdapterAddress**</span><span class="sxs-lookup"><span data-stu-id="1ce08-131">**AdapterAddress**</span></span>
</dt> <dd>

<span data-ttu-id="1ce08-132">Endereço NIC.</span><span class="sxs-lookup"><span data-stu-id="1ce08-132">NIC address.</span></span>

</dd> <dt>

<span data-ttu-id="1ce08-133">**WMachineName**</span><span class="sxs-lookup"><span data-stu-id="1ce08-133">**WMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="1ce08-134">Nome do computador Unicode.</span><span class="sxs-lookup"><span data-stu-id="1ce08-134">Unicode computer name.</span></span> <span data-ttu-id="1ce08-135">Este membro se aplica ao Monitor de Rede 2,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="1ce08-135">This member applies to Network Monitor 2.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="1ce08-136">**WUserName**</span><span class="sxs-lookup"><span data-stu-id="1ce08-136">**WUserName**</span></span>
</dt> <dd>

<span data-ttu-id="1ce08-137">Nome de usuário Unicode.</span><span class="sxs-lookup"><span data-stu-id="1ce08-137">Unicode user name.</span></span> <span data-ttu-id="1ce08-138">Este membro se aplica ao Monitor de Rede 2,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="1ce08-138">This member applies to Network Monitor 2.0 or later.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ce08-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ce08-139">Remarks</span></span>

<span data-ttu-id="1ce08-140">Uma matriz dessas estruturas é usada pela estrutura de tabela de [consulta](querytable.md) para fornecer uma lista dos computadores que atualmente estão usando monitor de rede para capturar dados.</span><span class="sxs-lookup"><span data-stu-id="1ce08-140">An array of these structures is used by the [QUERYTABLE](querytable.md) structure to provide a list of the computers that are currently using Network Monitor to capture data.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ce08-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ce08-141">Requirements</span></span>



| <span data-ttu-id="1ce08-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ce08-142">Requirement</span></span> | <span data-ttu-id="1ce08-143">Valor</span><span class="sxs-lookup"><span data-stu-id="1ce08-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1ce08-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ce08-144">Minimum supported client</span></span><br/> | <span data-ttu-id="1ce08-145">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ce08-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1ce08-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ce08-146">Minimum supported server</span></span><br/> | <span data-ttu-id="1ce08-147">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ce08-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1ce08-148">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1ce08-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ce08-149"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ce08-149"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ce08-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ce08-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ce08-151">CONSULTA</span><span class="sxs-lookup"><span data-stu-id="1ce08-151">QUERYTABLE</span></span>](querytable.md)
</dt> </dl>

 

 




