---
description: O método de transferência do objeto item transfere dados de um dispositivo para um arquivo. Esse método aplica-se somente a itens de tipo de dispositivo.
ms.assetid: ed9696da-bd94-4063-80c2-311a7a441b10
title: Método item. Transfer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Transfer
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: a476f9653b7deced48394af0ecaa0ea0c8ae51e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783767"
---
# <a name="itemtransfer-method"></a><span data-ttu-id="a725f-104">Método item. Transfer</span><span class="sxs-lookup"><span data-stu-id="a725f-104">Item.Transfer method</span></span>

<span data-ttu-id="a725f-105">O método de **transferência** do objeto [**Item**](-wia-item.md) transfere dados de um dispositivo para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a725f-105">The **Transfer** method of the [**Item**](-wia-item.md) object transfers data from a device to a file.</span></span> <span data-ttu-id="a725f-106">Esse método aplica-se somente a itens de tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a725f-106">This method applies only to device type items.</span></span>

## <a name="syntax"></a><span data-ttu-id="a725f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a725f-107">Syntax</span></span>


```JScript
Item.Transfer(
  Filename,
  AsyncTransfer = VARIANT_BOOL
)
```



## <a name="parameters"></a><span data-ttu-id="a725f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a725f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a725f-109">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a725f-109">*Filename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a725f-110">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a725f-110">Type: **BSTR**</span></span>

<span data-ttu-id="a725f-111">Especifica o nome do arquivo para o qual os dados são transferidos.</span><span class="sxs-lookup"><span data-stu-id="a725f-111">Specifies the name of the file to which the data is transferred.</span></span>

</dd> <dt>

<span data-ttu-id="a725f-112">*AsyncTransfer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a725f-112">*AsyncTransfer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a725f-113">Tipo: **\_ booliano de variante**</span><span class="sxs-lookup"><span data-stu-id="a725f-113">Type: **VARIANT\_BOOL**</span></span>

<span data-ttu-id="a725f-114">Um valor booliano que especifica se a transferência deve ser executada como uma chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="a725f-114">A Boolean value that specifies whether the transfer should be run as an asynchronous call.</span></span>

<dt>



 <span data-ttu-id="a725f-115">(Variante \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="a725f-115">(VARIANT\_BOOL)</span></span>


</dt> <dd>

<span data-ttu-id="a725f-116">Padrão.</span><span class="sxs-lookup"><span data-stu-id="a725f-116">Default.</span></span> <span data-ttu-id="a725f-117">Defina esse valor como **true** se a chamada deve ser assíncrona (consulte **comentários**).</span><span class="sxs-lookup"><span data-stu-id="a725f-117">Set this value to **true** if the call should be asynchronous (see **Remarks**).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a725f-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a725f-118">Return value</span></span>

<span data-ttu-id="a725f-119">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a725f-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a725f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="a725f-120">Remarks</span></span>

<span data-ttu-id="a725f-121">Esse método aplica-se somente a itens de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="a725f-121">This method applies only to file type items.</span></span> <span data-ttu-id="a725f-122">O método verifica se o item dá suporte a esse método antes de tentar concluir a transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="a725f-122">The method checks that the item supports this method before it attempts to complete the data transfer.</span></span>

<span data-ttu-id="a725f-123">Use "Clipboard" como o parâmetro *filename* para transferir um item para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="a725f-123">Use "clipboard" as the *Filename* parameter to transfer an item to the clipboard.</span></span>

<span data-ttu-id="a725f-124">Defina o valor de *AsyncTransfer* como **false** para transferências em qualquer aplicativo ou script executado em um ambiente que termine um processo no final de um script, como o WSH (Windows Script Host).</span><span class="sxs-lookup"><span data-stu-id="a725f-124">Set the *AsyncTransfer* value to **false** for transfers within any application or script that runs in an environment that terminates a process at the end of a script, such as Windows Script Host (WSH).</span></span> <span data-ttu-id="a725f-125">Caso contrário, o script pode terminar e o processo é encerrado antes de a transferência ser concluída.</span><span class="sxs-lookup"><span data-stu-id="a725f-125">Otherwise, the script may end, and the process terminate, before the transfer completes.</span></span>

<span data-ttu-id="a725f-126">O método de **transferência** não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="a725f-126">The **Transfer** method has no return value.</span></span> <span data-ttu-id="a725f-127">Após a conclusão de uma transferência, esse método envia um evento [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md) para o script ou aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a725f-127">Upon completion of a transfer, this method sends an [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md) event to the script or application.</span></span>

## <a name="examples"></a><span data-ttu-id="a725f-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a725f-128">Examples</span></span>

<span data-ttu-id="a725f-129">O exemplo a seguir demonstra o uso do método de **transferência** para transferir dados de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a725f-129">The following example demonstrates the use of the **Transfer** method to transfer data from a device.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItems
        objItem.Transfer("c:\Folder\Filename.bmp")
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="a725f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a725f-130">Requirements</span></span>



| <span data-ttu-id="a725f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a725f-131">Requirement</span></span> | <span data-ttu-id="a725f-132">Valor</span><span class="sxs-lookup"><span data-stu-id="a725f-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a725f-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a725f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a725f-134">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a725f-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a725f-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a725f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a725f-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a725f-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a725f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a725f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a725f-138"><dt>Wiascr.dll (versão 4,90 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="a725f-138"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




