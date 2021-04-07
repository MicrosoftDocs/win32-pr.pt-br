---
title: MCI_SYSINFO comando (mmsystem. h)
description: O comando do sysinfo do MCI \_ recupera informações sobre dispositivos MCI.
ms.assetid: 605efd25-8849-42aa-99fd-b36b6fd2c7b7
keywords:
- Multimídia do Windows de comando MCI_SYSINFO
topic_type:
- apiref
api_name:
- MCI_SYSINFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e722625449893771726a83738c3b0d7bc8bc523c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918558"
---
# <a name="mci_sysinfo-command"></a><span data-ttu-id="1be75-104">Comando do sysinfo do MCI \_</span><span class="sxs-lookup"><span data-stu-id="1be75-104">MCI\_SYSINFO command</span></span>

<span data-ttu-id="1be75-105">O comando do sysinfo do MCI \_ recupera informações sobre dispositivos MCI.</span><span class="sxs-lookup"><span data-stu-id="1be75-105">The MCI\_SYSINFO command retrieves information about MCI devices.</span></span> <span data-ttu-id="1be75-106">O MCI dá suporte a esse comando diretamente, em vez de passá-lo para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1be75-106">MCI supports this command directly rather than passing it to the device.</span></span> <span data-ttu-id="1be75-107">Qualquer aplicativo MCI pode usar esse comando.</span><span class="sxs-lookup"><span data-stu-id="1be75-107">Any MCI application can use this command.</span></span> <span data-ttu-id="1be75-108">As informações de cadeia de caracteres são retornadas no buffer fornecido pelo aplicativo apontado pelo membro **lpstrReturn** da estrutura identificada por *lpSysInfo*.</span><span class="sxs-lookup"><span data-stu-id="1be75-108">String information is returned in the application-supplied buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span> <span data-ttu-id="1be75-109">Informações numéricas são retornadas como um valor **DWORD** colocado no buffer fornecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1be75-109">Numeric information is returned as a **DWORD** value placed in the application-supplied buffer.</span></span> <span data-ttu-id="1be75-110">O membro **dwRetSize** especifica o comprimento do buffer.</span><span class="sxs-lookup"><span data-stu-id="1be75-110">The **dwRetSize** member specifies the buffer length.</span></span>

<span data-ttu-id="1be75-111">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="1be75-111">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SYSINFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SYSINFO_PARMS) lpSysInfo
);
```



## <a name="parameters"></a><span data-ttu-id="1be75-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1be75-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1be75-113"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="1be75-113"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="1be75-114">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="1be75-114">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="1be75-115"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="1be75-115"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="1be75-116">Um ou mais dos seguintes sinalizadores padrão e específicos de comando:</span><span class="sxs-lookup"><span data-stu-id="1be75-116">One or more of the following standard and command-specific flags:</span></span>

</dd> <dt>

<span data-ttu-id="1be75-117"><span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>instalação do do sysinfo do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="1be75-117"><span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>MCI\_SYSINFO\_INSTALLNAME</span></span>
</dt> <dd>

<span data-ttu-id="1be75-118">Obtém o nome (listado no registro ou o arquivo de SYSTEM.INI) usado para instalar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1be75-118">Obtains the name (listed in the registry or the SYSTEM.INI file) used to install the device.</span></span>

</dd> <dt>

<span data-ttu-id="1be75-119"><span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>\_nome do sysinfo do MCI \_</span><span class="sxs-lookup"><span data-stu-id="1be75-119"><span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>MCI\_SYSINFO\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="1be75-120">Obtém um nome de dispositivo correspondente ao número do dispositivo especificado no membro **dwNumber** da estrutura identificada por **lpSysInfo**.</span><span class="sxs-lookup"><span data-stu-id="1be75-120">Obtains a device name corresponding to the device number specified in the **dwNumber** member of the structure identified by **lpSysInfo**.</span></span> <span data-ttu-id="1be75-121">Se o sinalizador de abertura do sysinfo do MCI \_ \_ estiver definido, o MCI retornará os nomes dos dispositivos abertos.</span><span class="sxs-lookup"><span data-stu-id="1be75-121">If the MCI\_SYSINFO\_OPEN flag is set, MCI returns the names of open devices.</span></span>

</dd> <dt>

<span data-ttu-id="1be75-122"><span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>\_Open sysinfo do MCI \_</span><span class="sxs-lookup"><span data-stu-id="1be75-122"><span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>MCI\_SYSINFO\_OPEN</span></span>
</dt> <dd>

<span data-ttu-id="1be75-123">Obtém a quantidade ou o nome dos dispositivos abertos.</span><span class="sxs-lookup"><span data-stu-id="1be75-123">Obtains the quantity or name of open devices.</span></span>

</dd> <dt>

<span data-ttu-id="1be75-124"><span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>\_quantidade de sysinfo do MCI \_</span><span class="sxs-lookup"><span data-stu-id="1be75-124"><span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>MCI\_SYSINFO\_QUANTITY</span></span>
</dt> <dd>

<span data-ttu-id="1be75-125">Obtém o número de dispositivos do tipo especificado que estão listados no registro ou na \[ \] seção MCI do arquivo de SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="1be75-125">Obtains the number of devices of the specified type that are listed in the registry or the \[mci\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="1be75-126">Se o sinalizador de abertura do sysinfo do MCI \_ \_ estiver definido, o número de dispositivos abertos será retornado.</span><span class="sxs-lookup"><span data-stu-id="1be75-126">If the MCI\_SYSINFO\_OPEN flag is set, the number of open devices is returned.</span></span>

</dd> <dt>

<span data-ttu-id="1be75-127"><span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpSysInfo*</span><span class="sxs-lookup"><span data-stu-id="1be75-127"><span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpSysInfo*</span></span>
</dt> <dd>

<span data-ttu-id="1be75-128">Ponteiro para uma estrutura [**MCI de \_ \_ parâmetros do sysinfo**](mci-sysinfo-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="1be75-128">Pointer to an [**MCI\_SYSINFO\_PARMS**](mci-sysinfo-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1be75-129">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="1be75-129">Return Value</span></span>

<span data-ttu-id="1be75-130">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="1be75-130">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1be75-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="1be75-131">Remarks</span></span>

<span data-ttu-id="1be75-132">O membro **wDeviceType** da estrutura identificada por *lpSysInfo* é usado para indicar o tipo de dispositivo da consulta.</span><span class="sxs-lookup"><span data-stu-id="1be75-132">The **wDeviceType** member of the structure identified by *lpSysInfo* is used to indicate the device type of the query.</span></span> <span data-ttu-id="1be75-133">Se o parâmetro *wDeviceID* for definido como MCI \_ todos \_ os \_ IDs de dispositivo, ele substituirá o valor de **wDeviceType**.</span><span class="sxs-lookup"><span data-stu-id="1be75-133">If the *wDeviceID* parameter is set to MCI\_ALL\_DEVICE\_ID, it overrides the value of **wDeviceType**.</span></span> <span data-ttu-id="1be75-134">Para obter uma lista de tipos de dispositivo, consulte [tipos de dispositivo MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="1be75-134">For a list of device types, see [MCI Device Types](mci-device-types.md).</span></span>

<span data-ttu-id="1be75-135">Valores de retorno de inteiros são valores **DWORD** retornados no buffer apontados pelo membro **lpstrReturn** da estrutura identificada por *lpSysInfo*.</span><span class="sxs-lookup"><span data-stu-id="1be75-135">Integer return values are **DWORD** values returned in the buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span>

<span data-ttu-id="1be75-136">Os valores de retorno de String são cadeias de caracteres terminadas em nulo retornadas no buffer apontado pelo membro **lpstrReturn** da estrutura identificada por *lpSysInfo*.</span><span class="sxs-lookup"><span data-stu-id="1be75-136">String return values are null-terminated strings returned in the buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span>

## <a name="requirements"></a><span data-ttu-id="1be75-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1be75-137">Requirements</span></span>



| <span data-ttu-id="1be75-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="1be75-138">Requirement</span></span> | <span data-ttu-id="1be75-139">Valor</span><span class="sxs-lookup"><span data-stu-id="1be75-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1be75-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1be75-140">Minimum supported client</span></span><br/> | <span data-ttu-id="1be75-141">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1be75-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1be75-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1be75-142">Minimum supported server</span></span><br/> | <span data-ttu-id="1be75-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1be75-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1be75-144">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1be75-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="1be75-145"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1be75-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1be75-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="1be75-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1be75-147">MCI</span><span class="sxs-lookup"><span data-stu-id="1be75-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1be75-148">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="1be75-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

