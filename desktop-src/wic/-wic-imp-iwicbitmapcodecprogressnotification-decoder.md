---
description: Implementando IWICBitmapCodecProgressNotification (decodificador)
ms.assetid: 686b0875-c7ec-45ee-bd3e-94bfd9e5dcda
title: Implementando IWICBitmapCodecProgressNotification (decodificador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f05f02e77886d96d794be3f974c1eb0eed9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785200"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-decoder"></a><span data-ttu-id="0a93d-103">Implementando IWICBitmapCodecProgressNotification (decodificador)</span><span class="sxs-lookup"><span data-stu-id="0a93d-103">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>

## <a name="iwicbitmapcodecprogressnotification"></a><span data-ttu-id="0a93d-104">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="0a93d-104">IWICBitmapCodecProgressNotification</span></span>

<span data-ttu-id="0a93d-105">Quando um codec está executando uma operação de e/s como [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) em uma imagem grande, pode levar vários segundos ou até minutos para ser concluído.</span><span class="sxs-lookup"><span data-stu-id="0a93d-105">When a codec is performing an I/O operation such as [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) on a large image, it may take several seconds or even minutes to complete.</span></span> <span data-ttu-id="0a93d-106">Quando os usuários finais não conseguem interromper uma operação de execução longa, eles podem imaginar que o aplicativo foi suspenso.</span><span class="sxs-lookup"><span data-stu-id="0a93d-106">When end users are unable to interrupt a long-running operation, they may think the application has hung.</span></span> <span data-ttu-id="0a93d-107">Os usuários geralmente fecham um aplicativo ou até mesmo reiniciam seus computadores, em uma tentativa de reobter o controle do computador quando um aplicativo deixa de responder.</span><span class="sxs-lookup"><span data-stu-id="0a93d-107">Users will often close an application, or even restart their computers, in an attempt to regain control of their computer when an application becomes unresponsive.</span></span>

<span data-ttu-id="0a93d-108">Essa interface permite que um aplicativo especifique uma função de retorno de chamada que o codec pode chamar em intervalos especificados para notificar o chamador do progresso da operação atual.</span><span class="sxs-lookup"><span data-stu-id="0a93d-108">This interface enables an application to specify a callback function that the codec can call at specified intervals to notify the caller of the progress of the current operation.</span></span> <span data-ttu-id="0a93d-109">O aplicativo pode usar essa função de retorno de chamada para exibir uma indicação de progresso na interface do usuário para notificar o usuário sobre o status da operação.</span><span class="sxs-lookup"><span data-stu-id="0a93d-109">The application can use this callback function to display an indication of progress in the user interface to notify the user of the status of the operation.</span></span> <span data-ttu-id="0a93d-110">Se um usuário clicar no botão **Cancelar** na caixa de diálogo **progresso** , o aplicativo retornará **WINCODEC \_ erro \_ anulado** da função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="0a93d-110">If a user clicks the **Cancel** button on the **Progress** dialog box, the application returns **WINCODEC\_ERR\_ABORTED** from the callback function.</span></span> <span data-ttu-id="0a93d-111">Quando isso acontece, o codec deve cancelar a operação especificada e propagar esse **HRESULT** de volta para o chamador do método que estava executando a operação.</span><span class="sxs-lookup"><span data-stu-id="0a93d-111">When this happens, the codec must cancel the specified operation and propagate this **HRESULT** back to the caller of the method that was performing the operation.</span></span>

<span data-ttu-id="0a93d-112">Essa interface deve ser implementada em sua classe de decodificador de nível de contêiner.</span><span class="sxs-lookup"><span data-stu-id="0a93d-112">This interface should be implemented on your container-level decoder class.</span></span>


```C++
interface IWICBitmapCodecProgressNotification : public IUnknown
{
    HRESULT RegisterProgressNotification ( 
        PFNProgressNotification pfnProgressNotification,
        LPVOID pvData,
        DWORD dwProgressFlags );
}
```



-   [<span data-ttu-id="0a93d-113">RegisterProgressNotification</span><span class="sxs-lookup"><span data-stu-id="0a93d-113">RegisterProgressNotification</span></span>](#registerprogressnotification)
-   [<span data-ttu-id="0a93d-114">PFNProgressNotification</span><span class="sxs-lookup"><span data-stu-id="0a93d-114">PFNProgressNotification</span></span>](#pfnprogressnotification)

### <a name="registerprogressnotification"></a><span data-ttu-id="0a93d-115">RegisterProgressNotification</span><span class="sxs-lookup"><span data-stu-id="0a93d-115">RegisterProgressNotification</span></span>

<span data-ttu-id="0a93d-116">[**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) é invocado por um aplicativo para registrar uma função de retorno de chamada que o codec pode chamar em intervalos especificados.</span><span class="sxs-lookup"><span data-stu-id="0a93d-116">[**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) is invoked by an application to register a callback function that the codec can call at specified intervals.</span></span> <span data-ttu-id="0a93d-117">O primeiro parâmetro, *pfnProgressNotification*, é um ponteiro para a função de retorno de chamada que o codec deve chamar em intervalos regulares.</span><span class="sxs-lookup"><span data-stu-id="0a93d-117">The first parameter, *pfnProgressNotification*, is a pointer to the callback function that the codec should call at regular intervals.</span></span>

<span data-ttu-id="0a93d-118">O parâmetro *pvData* aponta para algum objeto que o chamador deseja que o codec transmita de volta para a função de retorno de chamada sempre que a função de chamada de retorno for invocada.</span><span class="sxs-lookup"><span data-stu-id="0a93d-118">The *pvData* parameter points to some object that the caller wants the codec to pass back to the callback function whenever the callback function is invoked.</span></span> <span data-ttu-id="0a93d-119">Esse objeto pode ser qualquer coisa e não tem um significado específico para o codec.</span><span class="sxs-lookup"><span data-stu-id="0a93d-119">This object may be anything at all and has no particular significance to the codec.</span></span>

<span data-ttu-id="0a93d-120">O parâmetro *dwProgressFlags* especifica quando o codec deve chamar a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="0a93d-120">The *dwProgressFlags* parameter specifies when the codec should call the callback function.</span></span> <span data-ttu-id="0a93d-121">Uma função ou pode ser executada com duas enumerações para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0a93d-121">An OR function can be performed with two enumerations for this parameter.</span></span> <span data-ttu-id="0a93d-122">A enumeração [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) especifica se deve chamar a função de retorno de chamada durante a decodificação (**WICProgressOperationCopyPixels**), codificação (**WICProgerssOperationWritePixels**) ou ambos (**WICProgressOperationAll**).</span><span class="sxs-lookup"><span data-stu-id="0a93d-122">The [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) enum specifies whether to call the callback function during decoding (**WICProgressOperationCopyPixels**), encoding (**WICProgerssOperationWritePixels**), or both (**WICProgressOperationAll**).</span></span>


```C++
enum WICProgressOperation
{
   WICProgressOperationCopyPixels,
   WICProgerssOperationWritePixels,
   WICProgressOperationAll      
};
```



<span data-ttu-id="0a93d-123">O codec deve chamar a função de retorno de chamada em intervalos regulares durante a operação, mas o chamador pode especificar determinados requisitos.</span><span class="sxs-lookup"><span data-stu-id="0a93d-123">The codec should call the callback function at regular intervals throughout the operation, but the caller may specify certain requirements.</span></span> <span data-ttu-id="0a93d-124">A enumeração [**WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) indica em qual ponto da operação chamar a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="0a93d-124">The [**WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) enum indicates at which point in the operation to call the callback function.</span></span> <span data-ttu-id="0a93d-125">Se o chamador especificar **WICProgressNotificationBegin**, você deverá chamá-lo no início da operação (0,0).</span><span class="sxs-lookup"><span data-stu-id="0a93d-125">If the caller specifies **WICProgressNotificationBegin**, you must call it at the beginning of the operation (0.0).</span></span> <span data-ttu-id="0a93d-126">Se o chamador não especificar isso, será opcional.</span><span class="sxs-lookup"><span data-stu-id="0a93d-126">If the caller does not specify this, it is optional.</span></span> <span data-ttu-id="0a93d-127">Da mesma forma, se o chamador especificar **WICProgerssNotificationEnd**, você deverá chamá-lo quando a operação for concluída (1,0).</span><span class="sxs-lookup"><span data-stu-id="0a93d-127">Likewise, if the caller specifies **WICProgerssNotificationEnd**, you must call it when the operation is completed (1.0).</span></span> <span data-ttu-id="0a93d-128">Se o chamador especificar **WICProgressNotificationAll**, você deverá chamá-lo no início e no final, bem como em intervalos regulares durante a operação.</span><span class="sxs-lookup"><span data-stu-id="0a93d-128">If the caller specifies **WICProgressNotificationAll**, you must call it at the beginning and end, as well as at regular intervals throughout the operation.</span></span> <span data-ttu-id="0a93d-129">O chamador também pode especificar **WICProgerssNotificationFrequent**, que indica que eles desejam ser chamados de volta em intervalos frequentes, talvez após cada duas linhas de verificação.</span><span class="sxs-lookup"><span data-stu-id="0a93d-129">The caller may also specify **WICProgerssNotificationFrequent**, which indicates that they want to be called back at frequent intervals, perhaps after every couple of scan lines.</span></span> <span data-ttu-id="0a93d-130">(Um chamador geralmente usará esse sinalizador apenas para uma imagem muito grande.) Caso contrário, você normalmente deve chamar de volta em intervalos de aproximadamente 10% de incrementos do número total de linhas de exame a serem processadas.</span><span class="sxs-lookup"><span data-stu-id="0a93d-130">(A caller will usually use this flag only for a very large image.) Otherwise, you should usually call back at intervals of approximately 10 percent increments of the total number of scan lines to be processed.</span></span>


```C++
enum WICProgressNotification
{
   WICProgressNotificationBegin,
   WICProgerssNotificationEnd,
   WICProgerssNotificationFrequent,
   WICProgressNotificationAll
};
```



<span data-ttu-id="0a93d-131">Somente uma função de retorno de chamada por vez pode ser registrada para um decodificador específico ou instância de codificador.</span><span class="sxs-lookup"><span data-stu-id="0a93d-131">Only one callback function at a time can be registered for a specific decoder or encoder instance.</span></span> <span data-ttu-id="0a93d-132">Se um aplicativo chamar [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) mais de uma vez, substitua a função de retorno de chamada anteriormente registrada pela nova.</span><span class="sxs-lookup"><span data-stu-id="0a93d-132">If an application calls [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) more than once, replace the previously registered callback function with the new one.</span></span> <span data-ttu-id="0a93d-133">Para cancelar um registro de retorno de chamada, um chamador definirá o parâmetro *pfnProgressNotification* como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0a93d-133">To cancel a callback registration, a caller will set the *pfnProgressNotification* parameter to **NULL**.</span></span>

### <a name="pfnprogressnotification"></a><span data-ttu-id="0a93d-134">PFNProgressNotification</span><span class="sxs-lookup"><span data-stu-id="0a93d-134">PFNProgressNotification</span></span>

<span data-ttu-id="0a93d-135">[**PFNProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) é a função de retorno de chamada com a assinatura a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a93d-135">[**PFNProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) is the callback function with the following signature.</span></span>


```C++
typedef HRESULT (*PFNProgressNotification) ( 
   LPVOID pvData,
   ULONG uFrameNum,
   WICProgressOperation operation,
   double dblProgress );
```



<span data-ttu-id="0a93d-136">Quando você invoca a função de retorno de chamada, use o parâmetro *pvData* para passar de volta o mesmo *pvData* que o aplicativo especificou quando registrou a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="0a93d-136">When you invoke the callback function, use the *pvData* parameter to pass back the same *pvData* that the application specified when it registered the callback function.</span></span>

<span data-ttu-id="0a93d-137">O parâmetro *uFrameNum* deve indicar o índice do quadro que está sendo processado.</span><span class="sxs-lookup"><span data-stu-id="0a93d-137">The *uFrameNum* parameter should indicate the index of the frame that is being processed.</span></span>

<span data-ttu-id="0a93d-138">Defina o parâmetro operation como **WICProgressOperationCopyPixels** ao decodificar e **WICProgressOperationWritePixels** ao codificar.</span><span class="sxs-lookup"><span data-stu-id="0a93d-138">Set the operation parameter to **WICProgressOperationCopyPixels** when decoding and **WICProgressOperationWritePixels** when encoding.</span></span>

<span data-ttu-id="0a93d-139">O parâmetro *dblProgress* deve ser um número entre 0,0 (o início da operação) e 1,0 (a conclusão da operação).</span><span class="sxs-lookup"><span data-stu-id="0a93d-139">The *dblProgress* parameter should be a number between 0.0 (the beginning of the operation) and 1.0 (the completion of the operation).</span></span> <span data-ttu-id="0a93d-140">O valor deve refletir a proporção de linhas de verificação já processadas em relação ao número total de linhas de exame a serem processadas.</span><span class="sxs-lookup"><span data-stu-id="0a93d-140">The value should reflect the proportion of scan lines already processed relative to the total number of scan lines to be processed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a93d-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a93d-141">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0a93d-142">**Referência**</span><span class="sxs-lookup"><span data-stu-id="0a93d-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0a93d-143">**ProgressNotificationCallback**</span><span class="sxs-lookup"><span data-stu-id="0a93d-143">**ProgressNotificationCallback**</span></span>](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)
</dt> <dt>

[<span data-ttu-id="0a93d-144">**IWICBitmapCodecProgressNotification**</span><span class="sxs-lookup"><span data-stu-id="0a93d-144">**IWICBitmapCodecProgressNotification**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification)
</dt> <dt>

<span data-ttu-id="0a93d-145">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="0a93d-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0a93d-146">Implementando IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="0a93d-146">Implementing IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[<span data-ttu-id="0a93d-147">Implementando IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="0a93d-147">Implementing IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[<span data-ttu-id="0a93d-148">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="0a93d-148">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="0a93d-149">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="0a93d-149">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



