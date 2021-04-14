---
description: Um processo usa a função CreateFile para abrir um identificador para um recurso de comunicação.
ms.assetid: eaef6067-97a6-40c4-84ec-c0d86af6bb4a
title: Identificadores de recursos de comunicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709fc041f6125d93a1c52f3e17b77c96f35825c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370434"
---
# <a name="communications-resource-handles"></a><span data-ttu-id="0697c-103">Identificadores de recursos de comunicação</span><span class="sxs-lookup"><span data-stu-id="0697c-103">Communications Resource Handles</span></span>

<span data-ttu-id="0697c-104">Um processo usa a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir um identificador para um recurso de comunicação.</span><span class="sxs-lookup"><span data-stu-id="0697c-104">A process uses the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a handle to a communications resource.</span></span> <span data-ttu-id="0697c-105">Por exemplo, a especificação de COM1 abre um identificador para uma porta serial e a LPT1 abre um identificador para uma porta paralela.</span><span class="sxs-lookup"><span data-stu-id="0697c-105">For example, specifying COM1 opens a handle to a serial port, and LPT1 opens a handle to a parallel port.</span></span> <span data-ttu-id="0697c-106">Se o recurso especificado estiver sendo usado atualmente por outro processo, **CreateFile** falhará.</span><span class="sxs-lookup"><span data-stu-id="0697c-106">If the specified resource is currently being used by another process, **CreateFile** fails.</span></span> <span data-ttu-id="0697c-107">Qualquer thread do processo pode usar o identificador retornado por **CreateFile** para identificar o recurso em qualquer uma das funções que acessam o recurso.</span><span class="sxs-lookup"><span data-stu-id="0697c-107">Any thread of the process can use the handle returned by **CreateFile** to identify the resource in any of the functions that access the resource.</span></span>

<span data-ttu-id="0697c-108">Quando o processo chama [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir um recurso de comunicação, ele especifica os seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="0697c-108">When the process calls [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a communications resource, it specifies the following attributes:</span></span>

-   <span data-ttu-id="0697c-109">Que tipo de acesso de leitura/gravação existe para o recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="0697c-109">What type of read/write access exists for the specified resource.</span></span>
-   <span data-ttu-id="0697c-110">Se o identificador pode ser herdado por processos filho.</span><span class="sxs-lookup"><span data-stu-id="0697c-110">Whether the handle can be inherited by child processes.</span></span>
-   <span data-ttu-id="0697c-111">Se o identificador pode ser usado em operações de e/s sobrepostas (assíncronas).</span><span class="sxs-lookup"><span data-stu-id="0697c-111">Whether the handle can be used in overlapped (asynchronous) I/O operations.</span></span> <span data-ttu-id="0697c-112">(Para obter uma descrição das operações sobrepostas, consulte [sincronização](/windows/desktop/Sync/synchronization).)</span><span class="sxs-lookup"><span data-stu-id="0697c-112">(For a description of overlapped operations, see [Synchronization](/windows/desktop/Sync/synchronization).)</span></span>

<span data-ttu-id="0697c-113">Quando o processo usa [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir um recurso de comunicação, ele deve especificar determinados valores para os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="0697c-113">When the process uses [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a communications resource, it must specify certain values for the following parameters:</span></span>

-   <span data-ttu-id="0697c-114">O parâmetro *fdwShareMode* deve ser zero, abrindo o recurso para acesso exclusivo.</span><span class="sxs-lookup"><span data-stu-id="0697c-114">The *fdwShareMode* parameter must be zero, opening the resource for exclusive access.</span></span>
-   <span data-ttu-id="0697c-115">O parâmetro *fdwCreate* deve especificar o \_ sinalizador Open existing.</span><span class="sxs-lookup"><span data-stu-id="0697c-115">The *fdwCreate* parameter must specify the OPEN\_EXISTING flag.</span></span>
-   <span data-ttu-id="0697c-116">O parâmetro *hTemplateFile* deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0697c-116">The *hTemplateFile* parameter must be **NULL**.</span></span>

<span data-ttu-id="0697c-117">Ao usar [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir um identificador diretamente em um dispositivo, um aplicativo deve usar os caracteres especiais " \\ \\ . \\ " para identificar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0697c-117">When using [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a handle directly to a device, an application must use the special characters " \\\\ .\\" to identify the device.</span></span> <span data-ttu-id="0697c-118">Por exemplo, para abrir um identificador para a unidade A, especifique \\ \\ . \\ r: para o parâmetro *lpszName* de **CreateFile**.</span><span class="sxs-lookup"><span data-stu-id="0697c-118">For example, to open a handle to drive A, specify \\\\ .\\a: for the *lpszName* parameter of **CreateFile**.</span></span> <span data-ttu-id="0697c-119">O processo de chamada pode usar o identificador na função [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) para enviar códigos de controle para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0697c-119">The calling process can use the handle in the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function to send control codes to the device.</span></span>

 

 
