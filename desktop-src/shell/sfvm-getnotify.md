---
description: Notificação enviada ao objeto de retorno de chamada de exibição para especificar os locais e eventos que devem ser registrados para eventos de notificação de alteração.
title: Mensagem de SFVM_GETNOTIFY (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87933217-dfa9-4aaf-9630-fa2c302b18fa
api_name:
- SFVM_GETNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f766ee74463dd820c0b55d501d5002a3378a97b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170320"
---
# <a name="sfvm_getnotify-message"></a><span data-ttu-id="cae4f-103">Mensagem de SFVM \_ GETnotify</span><span class="sxs-lookup"><span data-stu-id="cae4f-103">SFVM\_GETNOTIFY message</span></span>

<span data-ttu-id="cae4f-104">Notificação enviada ao objeto de retorno de chamada de exibição para especificar os locais e eventos que devem ser registrados para eventos de notificação de alteração.</span><span class="sxs-lookup"><span data-stu-id="cae4f-104">Notification sent to the view callback object to specify the locations and events that should be registered for change notification events.</span></span> <span data-ttu-id="cae4f-105">Depois que eles são registrados, quando uma alteração ocorre no nesses locais ou eventos, o objeto exibir retorno de chamada é notificado.</span><span class="sxs-lookup"><span data-stu-id="cae4f-105">Once they are registered, when a change occurs in on of these locations or events, the view callback object is notified.</span></span> <span data-ttu-id="cae4f-106">Esses eventos são enviados para o retorno de chamada de exibição por meio de [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) e, em seguida, são tratados pelo modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="cae4f-106">These events are sent to the view callback through [**SFVM\_FSNOTIFY**](sfvm-fsnotify.md) and are then handled by the view.</span></span>


```C++
SFVM_GETNOTIFY 

    wParam = (WPARAM)(LPITEMIDLIST*) pidl;

    lParam = (LPARAM)(LONG*) lEvents;

            
```



## <a name="parameters"></a><span data-ttu-id="cae4f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cae4f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cae4f-108">*PIDL* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cae4f-108">*pidl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cae4f-109">Um ponteiro para um IDList absoluto de um item para o qual a exibição deve se registrar para ser notificado das alterações.</span><span class="sxs-lookup"><span data-stu-id="cae4f-109">A pointer to an absolute IDList of an item for which the view should register to be notified of changes.</span></span> <span data-ttu-id="cae4f-110">Normalmente, isso é o mesmo que o IDList do local que está sendo exibido, mas pode ser outro local.</span><span class="sxs-lookup"><span data-stu-id="cae4f-110">Typically, this is the same as the IDList of the location being viewed, but it can be another location.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cae4f-111">O tempo de vida desse valor é de Propriedade do objeto de retorno de chamada de exibição.</span><span class="sxs-lookup"><span data-stu-id="cae4f-111">The lifetime of this value is owned by the view callback object.</span></span> <span data-ttu-id="cae4f-112">É responsabilidade do objeto exibir retorno de chamada criar e, em seguida, liberar esse valor quando ele não for mais necessário.</span><span class="sxs-lookup"><span data-stu-id="cae4f-112">It is the responsibility of the view callback object to create and then free this value when it is no longer needed.</span></span> <span data-ttu-id="cae4f-113">Isso requer que o objeto de retorno de chamada de exibição armazene esse valor.</span><span class="sxs-lookup"><span data-stu-id="cae4f-113">This requires that the view callback object stores this value.</span></span> <span data-ttu-id="cae4f-114">Normalmente, o valor pode ser armazenado no membro **\_ pidlMonitor** do objeto View callback.</span><span class="sxs-lookup"><span data-stu-id="cae4f-114">Usually, the value can be stored in the **\_pidlMonitor** member of the view callback object.</span></span> <span data-ttu-id="cae4f-115">As regras de propriedade para o valor retornado por meio de *PIDL* não são padrão e exigem cuidados especiais.</span><span class="sxs-lookup"><span data-stu-id="cae4f-115">The ownership rules for the value returned through *pidl* are nonstandard and require special care.</span></span> <span data-ttu-id="cae4f-116">O objeto de retorno de chamada de exibição deve possuir esse valor e garantir que ele não seja liberado até que o objeto de retorno de chamada de exibição seja destruído.</span><span class="sxs-lookup"><span data-stu-id="cae4f-116">The view callback object must own this value and ensure that it is not freed until the view callback object itself is destroyed.</span></span>

 

</dd> <dt>

<span data-ttu-id="cae4f-117">*lEvents* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cae4f-117">*lEvents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cae4f-118">Um valor que contém um ou mais valores SHCNE.</span><span class="sxs-lookup"><span data-stu-id="cae4f-118">A value that contains one or more SHCNE values.</span></span> <span data-ttu-id="cae4f-119">Consulte [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) para obter uma lista de possíveis valores.</span><span class="sxs-lookup"><span data-stu-id="cae4f-119">See [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) for a list of possible values.</span></span> <span data-ttu-id="cae4f-120">O objeto exibir retorno de chamada será registrado para receber uma mensagem [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) quando qualquer um dos eventos associados ocorrer.</span><span class="sxs-lookup"><span data-stu-id="cae4f-120">The view callback object will register to receive an [**SFVM\_FSNOTIFY**](sfvm-fsnotify.md) message when any of the associated events occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cae4f-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cae4f-121">Return value</span></span>

<span data-ttu-id="cae4f-122">Ignorado, mas deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cae4f-122">Ignored, but should return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="cae4f-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="cae4f-123">Remarks</span></span>

<span data-ttu-id="cae4f-124">Se essa mensagem de retorno de chamada não retornar um valor diferente de zero para o IDList ou a máscara de eventos, a exibição não será registrada para notificações de alteração.</span><span class="sxs-lookup"><span data-stu-id="cae4f-124">If this callback message does not return a nonzero value for either the IDList or the events mask then the view will not register for change notifications.</span></span>

## <a name="examples"></a><span data-ttu-id="cae4f-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cae4f-125">Examples</span></span>

<span data-ttu-id="cae4f-126">O exemplo a seguir mostra uma implementação de exemplo do código do manipulador da função de retorno de chamada para **SFVM \_ getnotificate**.</span><span class="sxs-lookup"><span data-stu-id="cae4f-126">The following sample shows an example implementation of the view callback function's handler code for **SFVM\_GETNOTIFY**.</span></span>


```C++
case SFVM_GETNOTIFY:
  *((LPITEMIDLIST*)wParam) = _pidl;    // Pass a reference whose lifetime this 
                                       // class is responsible for.
                                      
  *((LONG*)lParam) = SHCNE_DISKEVENTS; // A combination of all of the 
                                       // disk event identifiers.
                                       
   return S_OK;
```



## <a name="requirements"></a><span data-ttu-id="cae4f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cae4f-127">Requirements</span></span>



| <span data-ttu-id="cae4f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cae4f-128">Requirement</span></span> | <span data-ttu-id="cae4f-129">Valor</span><span class="sxs-lookup"><span data-stu-id="cae4f-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cae4f-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cae4f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cae4f-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cae4f-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cae4f-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cae4f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cae4f-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cae4f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cae4f-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cae4f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="cae4f-135"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="cae4f-135"><dt>Shlobj.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cae4f-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="cae4f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cae4f-137">**SFVM \_ QUERYFSNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="cae4f-137">**SFVM\_QUERYFSNOTIFY**</span></span>](sfvm-queryfsnotify.md)
</dt> <dt>

[<span data-ttu-id="cae4f-138">**IShellFolderViewCB::MessageSFVCB**</span><span class="sxs-lookup"><span data-stu-id="cae4f-138">**IShellFolderViewCB::MessageSFVCB**</span></span>](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)
</dt> </dl>

 

 
