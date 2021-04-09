---
description: O Microsoft Windows fornece várias propriedades do sistema que você pode usar para seus formatos de arquivo.
ms.assetid: 3a25c4fb-ffea-4524-b59b-912416b2fc7d
title: Propriedades de System-Defined para formatos de arquivo personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1a3645e383ea751298f766eacf60f5ac95ece3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090055"
---
# <a name="system-defined-properties-for-custom-file-formats"></a><span data-ttu-id="c5303-103">Propriedades de System-Defined para formatos de arquivo personalizados</span><span class="sxs-lookup"><span data-stu-id="c5303-103">System-Defined Properties for Custom File Formats</span></span>

<span data-ttu-id="c5303-104">O Microsoft Windows fornece várias propriedades do sistema que você pode usar para seus formatos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c5303-104">Microsoft Windows supplies a number of system properties that you can use for your file formats.</span></span> <span data-ttu-id="c5303-105">Se você estiver criando um formato de arquivo personalizado, deverá oferecer suporte a tantas propriedades definidas pelo sistema quanto possível.</span><span class="sxs-lookup"><span data-stu-id="c5303-105">If you are creating a custom file format, you should support as many system-defined properties as you can.</span></span> <span data-ttu-id="c5303-106">Antes de criar um manipulador de propriedade personalizada, você deve revisar os manipuladores fornecidos pelo sistema para ver se você pode usar um em vez de escrever o seu próprio.</span><span class="sxs-lookup"><span data-stu-id="c5303-106">Before creating a custom property handler, you should review the system-supplied handlers to see if you can use one instead of writing your own.</span></span>

<span data-ttu-id="c5303-107">A tabela a seguir categoriza os formatos de arquivo e lista as propriedades de sistema mais importantes às quais o formato de arquivo deve dar suporte.</span><span class="sxs-lookup"><span data-stu-id="c5303-107">The following table categorizes file formats and then lists the most important system properties your file format should support.</span></span> <span data-ttu-id="c5303-108">Para fornecer uma boa experiência do usuário, você deve dar suporte a todas as propriedades de prioridade 1 e 2 para sua categoria de formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c5303-108">To provide a good user experience, you should support all priority 1 and 2 properties for your category of file format.</span></span>

-   [<span data-ttu-id="c5303-109">Comunicações</span><span class="sxs-lookup"><span data-stu-id="c5303-109">Communications</span></span>](#communications)
-   [<span data-ttu-id="c5303-110">Contatos</span><span class="sxs-lookup"><span data-stu-id="c5303-110">Contacts</span></span>](#contacts)
-   [<span data-ttu-id="c5303-111">Documentos</span><span class="sxs-lookup"><span data-stu-id="c5303-111">Documents</span></span>](#documents)
-   [<span data-ttu-id="c5303-112">Genérico</span><span class="sxs-lookup"><span data-stu-id="c5303-112">Generic</span></span>](#generic)
-   [<span data-ttu-id="c5303-113">Música</span><span class="sxs-lookup"><span data-stu-id="c5303-113">Music</span></span>](#music)
-   [<span data-ttu-id="c5303-114">Imagens</span><span class="sxs-lookup"><span data-stu-id="c5303-114">Pictures</span></span>](#pictures)
-   [<span data-ttu-id="c5303-115">Vídeos</span><span class="sxs-lookup"><span data-stu-id="c5303-115">Videos</span></span>](#videos)
-   [<span data-ttu-id="c5303-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c5303-116">Related topics</span></span>](#related-topics)

## <a name="communications"></a><span data-ttu-id="c5303-117">Comunicações</span><span class="sxs-lookup"><span data-stu-id="c5303-117">Communications</span></span>



| <span data-ttu-id="c5303-118">Nome</span><span class="sxs-lookup"><span data-stu-id="c5303-118">Name</span></span>            | <span data-ttu-id="c5303-119">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c5303-119">Property</span></span>                               | <span data-ttu-id="c5303-120">Prioridade</span><span class="sxs-lookup"><span data-stu-id="c5303-120">Priority</span></span> |
|-----------------|----------------------------------------|----------|
| <span data-ttu-id="c5303-121">Data de recebimento</span><span class="sxs-lookup"><span data-stu-id="c5303-121">Date received</span></span>   | <span data-ttu-id="c5303-122">System. Message. DateReceived</span><span class="sxs-lookup"><span data-stu-id="c5303-122">System.Message.DateReceived</span></span>            | <span data-ttu-id="c5303-123">1</span><span class="sxs-lookup"><span data-stu-id="c5303-123">1</span></span>        |
| <span data-ttu-id="c5303-124">Nomes de</span><span class="sxs-lookup"><span data-stu-id="c5303-124">From names</span></span>      | <span data-ttu-id="c5303-125">System. Message. FromName</span><span class="sxs-lookup"><span data-stu-id="c5303-125">System.Message.FromName</span></span>                | <span data-ttu-id="c5303-126">1</span><span class="sxs-lookup"><span data-stu-id="c5303-126">1</span></span>        |
| <span data-ttu-id="c5303-127">Tem anexos</span><span class="sxs-lookup"><span data-stu-id="c5303-127">Has attachments</span></span> | <span data-ttu-id="c5303-128">System. Message. HasAttachments</span><span class="sxs-lookup"><span data-stu-id="c5303-128">System.Message.HasAttachments</span></span>          | <span data-ttu-id="c5303-129">1</span><span class="sxs-lookup"><span data-stu-id="c5303-129">1</span></span>        |
| <span data-ttu-id="c5303-130">Mailbox</span><span class="sxs-lookup"><span data-stu-id="c5303-130">Mailbox</span></span>         | <span data-ttu-id="c5303-131">System. Communication. storeddisplayname</span><span class="sxs-lookup"><span data-stu-id="c5303-131">System.Communication.storeddisplayname</span></span> | <span data-ttu-id="c5303-132">1</span><span class="sxs-lookup"><span data-stu-id="c5303-132">1</span></span>        |
| <span data-ttu-id="c5303-133">Name</span><span class="sxs-lookup"><span data-stu-id="c5303-133">Name</span></span>            | <span data-ttu-id="c5303-134">System. FileName</span><span class="sxs-lookup"><span data-stu-id="c5303-134">System.FileName</span></span>                        | <span data-ttu-id="c5303-135">1</span><span class="sxs-lookup"><span data-stu-id="c5303-135">1</span></span>        |
| <span data-ttu-id="c5303-136">Assunto</span><span class="sxs-lookup"><span data-stu-id="c5303-136">Subject</span></span>         | <span data-ttu-id="c5303-137">Sistema. Subject</span><span class="sxs-lookup"><span data-stu-id="c5303-137">System.Subject</span></span>                         | <span data-ttu-id="c5303-138">1</span><span class="sxs-lookup"><span data-stu-id="c5303-138">1</span></span>        |
| <span data-ttu-id="c5303-139">Nomes para</span><span class="sxs-lookup"><span data-stu-id="c5303-139">To names</span></span>        | <span data-ttu-id="c5303-140">System. Message. NoName</span><span class="sxs-lookup"><span data-stu-id="c5303-140">System.Message.ToName</span></span>                  | <span data-ttu-id="c5303-141">1</span><span class="sxs-lookup"><span data-stu-id="c5303-141">1</span></span>        |
| <span data-ttu-id="c5303-142">Categoria</span><span class="sxs-lookup"><span data-stu-id="c5303-142">Category</span></span>        | <span data-ttu-id="c5303-143">System. Category</span><span class="sxs-lookup"><span data-stu-id="c5303-143">System.Category</span></span>                        | <span data-ttu-id="c5303-144">2</span><span class="sxs-lookup"><span data-stu-id="c5303-144">2</span></span>        |
| <span data-ttu-id="c5303-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5303-145">Type</span></span>            | <span data-ttu-id="c5303-146">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="c5303-146">System.PerceivedType</span></span>                   | <span data-ttu-id="c5303-147">2</span><span class="sxs-lookup"><span data-stu-id="c5303-147">2</span></span>        |



 

## <a name="contacts"></a><span data-ttu-id="c5303-148">Contatos</span><span class="sxs-lookup"><span data-stu-id="c5303-148">Contacts</span></span>



| <span data-ttu-id="c5303-149">Nome</span><span class="sxs-lookup"><span data-stu-id="c5303-149">Name</span></span>             | <span data-ttu-id="c5303-150">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c5303-150">Property</span></span>                           | <span data-ttu-id="c5303-151">Prioridade</span><span class="sxs-lookup"><span data-stu-id="c5303-151">Priority</span></span> |
|------------------|------------------------------------|----------|
| <span data-ttu-id="c5303-152">Nome da Conta</span><span class="sxs-lookup"><span data-stu-id="c5303-152">Account Name</span></span>     | <span data-ttu-id="c5303-153">System. Communication. AccountName</span><span class="sxs-lookup"><span data-stu-id="c5303-153">System.Communication.AccountName</span></span>   | <span data-ttu-id="c5303-154">1</span><span class="sxs-lookup"><span data-stu-id="c5303-154">1</span></span>        |
| <span data-ttu-id="c5303-155">Telefone comercial</span><span class="sxs-lookup"><span data-stu-id="c5303-155">Business Phone</span></span>   | <span data-ttu-id="c5303-156">System. Contact. BusinessTelephone</span><span class="sxs-lookup"><span data-stu-id="c5303-156">System.Contact.BusinessTelephone</span></span>   | <span data-ttu-id="c5303-157">1</span><span class="sxs-lookup"><span data-stu-id="c5303-157">1</span></span>        |
| <span data-ttu-id="c5303-158">Empresa</span><span class="sxs-lookup"><span data-stu-id="c5303-158">Company</span></span>          | <span data-ttu-id="c5303-159">System. Company</span><span class="sxs-lookup"><span data-stu-id="c5303-159">System.Company</span></span>                     | <span data-ttu-id="c5303-160">1</span><span class="sxs-lookup"><span data-stu-id="c5303-160">1</span></span>        |
| <span data-ttu-id="c5303-161">Endereço de Email</span><span class="sxs-lookup"><span data-stu-id="c5303-161">Email Address</span></span>    | <span data-ttu-id="c5303-162">System. Contact. PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="c5303-162">System.Contact.PrimaryEmailAddress</span></span> | <span data-ttu-id="c5303-163">1</span><span class="sxs-lookup"><span data-stu-id="c5303-163">1</span></span>        |
| <span data-ttu-id="c5303-164">Importância</span><span class="sxs-lookup"><span data-stu-id="c5303-164">Importance</span></span>       | <span data-ttu-id="c5303-165">System. ImportanceText</span><span class="sxs-lookup"><span data-stu-id="c5303-165">System.ImportanceText</span></span>              | <span data-ttu-id="c5303-166">1</span><span class="sxs-lookup"><span data-stu-id="c5303-166">1</span></span>        |
| <span data-ttu-id="c5303-167">Telefone celular</span><span class="sxs-lookup"><span data-stu-id="c5303-167">Mobile Phone</span></span>     | <span data-ttu-id="c5303-168">System. Contact. MobileTelephone</span><span class="sxs-lookup"><span data-stu-id="c5303-168">System.Contact.MobileTelephone</span></span>     | <span data-ttu-id="c5303-169">1</span><span class="sxs-lookup"><span data-stu-id="c5303-169">1</span></span>        |
| <span data-ttu-id="c5303-170">Endereço comercial</span><span class="sxs-lookup"><span data-stu-id="c5303-170">Business address</span></span> | <span data-ttu-id="c5303-171">System. Contact. BusinessAddress</span><span class="sxs-lookup"><span data-stu-id="c5303-171">System.Contact.BusinessAddress</span></span>     | <span data-ttu-id="c5303-172">2</span><span class="sxs-lookup"><span data-stu-id="c5303-172">2</span></span>        |
| <span data-ttu-id="c5303-173">Fax comercial</span><span class="sxs-lookup"><span data-stu-id="c5303-173">Business fax</span></span>     | <span data-ttu-id="c5303-174">System. Contact. BusinessFaxNumber</span><span class="sxs-lookup"><span data-stu-id="c5303-174">System.Contact.BusinessFaxNumber</span></span>   | <span data-ttu-id="c5303-175">2</span><span class="sxs-lookup"><span data-stu-id="c5303-175">2</span></span>        |
| <span data-ttu-id="c5303-176">Categoria</span><span class="sxs-lookup"><span data-stu-id="c5303-176">Category</span></span>         | <span data-ttu-id="c5303-177">System. Category</span><span class="sxs-lookup"><span data-stu-id="c5303-177">System.Category</span></span>                    | <span data-ttu-id="c5303-178">2</span><span class="sxs-lookup"><span data-stu-id="c5303-178">2</span></span>        |
| <span data-ttu-id="c5303-179">Endereço residencial</span><span class="sxs-lookup"><span data-stu-id="c5303-179">Home address</span></span>     | <span data-ttu-id="c5303-180">System. Contact. HomeAddress</span><span class="sxs-lookup"><span data-stu-id="c5303-180">System.Contact.HomeAddress</span></span>         | <span data-ttu-id="c5303-181">2</span><span class="sxs-lookup"><span data-stu-id="c5303-181">2</span></span>        |
| <span data-ttu-id="c5303-182">Telefone residencial</span><span class="sxs-lookup"><span data-stu-id="c5303-182">Home phone</span></span>       | <span data-ttu-id="c5303-183">System. Contact. HomeTelephone</span><span class="sxs-lookup"><span data-stu-id="c5303-183">System.Contact.HomeTelephone</span></span>       | <span data-ttu-id="c5303-184">2</span><span class="sxs-lookup"><span data-stu-id="c5303-184">2</span></span>        |
| <span data-ttu-id="c5303-185">Título</span><span class="sxs-lookup"><span data-stu-id="c5303-185">Title</span></span>            | <span data-ttu-id="c5303-186">System.Title</span><span class="sxs-lookup"><span data-stu-id="c5303-186">System.Title</span></span>                       | <span data-ttu-id="c5303-187">2</span><span class="sxs-lookup"><span data-stu-id="c5303-187">2</span></span>        |



 

## <a name="documents"></a><span data-ttu-id="c5303-188">Documentos</span><span class="sxs-lookup"><span data-stu-id="c5303-188">Documents</span></span>



| <span data-ttu-id="c5303-189">Nome</span><span class="sxs-lookup"><span data-stu-id="c5303-189">Name</span></span>      | <span data-ttu-id="c5303-190">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c5303-190">Property</span></span>             | <span data-ttu-id="c5303-191">Prioridade</span><span class="sxs-lookup"><span data-stu-id="c5303-191">Priority</span></span> |
|-----------|----------------------|----------|
| <span data-ttu-id="c5303-192">Autores</span><span class="sxs-lookup"><span data-stu-id="c5303-192">Authors</span></span>   | <span data-ttu-id="c5303-193">System.Author</span><span class="sxs-lookup"><span data-stu-id="c5303-193">System.Author</span></span>        | <span data-ttu-id="c5303-194">1</span><span class="sxs-lookup"><span data-stu-id="c5303-194">1</span></span>        |
| <span data-ttu-id="c5303-195">Texto Completo</span><span class="sxs-lookup"><span data-stu-id="c5303-195">Full Text</span></span> | <span data-ttu-id="c5303-196">Sistema. FullText</span><span class="sxs-lookup"><span data-stu-id="c5303-196">System.FullText</span></span>      | <span data-ttu-id="c5303-197">1</span><span class="sxs-lookup"><span data-stu-id="c5303-197">1</span></span>        |
| <span data-ttu-id="c5303-198">Marcas</span><span class="sxs-lookup"><span data-stu-id="c5303-198">Tags</span></span>      | <span data-ttu-id="c5303-199">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="c5303-199">System.Keywords</span></span>      | <span data-ttu-id="c5303-200">1</span><span class="sxs-lookup"><span data-stu-id="c5303-200">1</span></span>        |
| <span data-ttu-id="c5303-201">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5303-201">Type</span></span>      | <span data-ttu-id="c5303-202">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="c5303-202">System.PerceivedType</span></span> | <span data-ttu-id="c5303-203">1</span><span class="sxs-lookup"><span data-stu-id="c5303-203">1</span></span>        |
| <span data-ttu-id="c5303-204">Categoria</span><span class="sxs-lookup"><span data-stu-id="c5303-204">Category</span></span>  | <span data-ttu-id="c5303-205">System. Category</span><span class="sxs-lookup"><span data-stu-id="c5303-205">System.Category</span></span>      | <span data-ttu-id="c5303-206">2</span><span class="sxs-lookup"><span data-stu-id="c5303-206">2</span></span>        |
| <span data-ttu-id="c5303-207">Título</span><span class="sxs-lookup"><span data-stu-id="c5303-207">Title</span></span>     | <span data-ttu-id="c5303-208">System.Title</span><span class="sxs-lookup"><span data-stu-id="c5303-208">System.Title</span></span>         | <span data-ttu-id="c5303-209">2</span><span class="sxs-lookup"><span data-stu-id="c5303-209">2</span></span>        |



 

## <a name="generic"></a><span data-ttu-id="c5303-210">Genérico</span><span class="sxs-lookup"><span data-stu-id="c5303-210">Generic</span></span>



| <span data-ttu-id="c5303-211">Nome</span><span class="sxs-lookup"><span data-stu-id="c5303-211">Name</span></span>     | <span data-ttu-id="c5303-212">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c5303-212">Property</span></span>             | <span data-ttu-id="c5303-213">Prioridade</span><span class="sxs-lookup"><span data-stu-id="c5303-213">Priority</span></span> |
|----------|----------------------|----------|
| <span data-ttu-id="c5303-214">Autores</span><span class="sxs-lookup"><span data-stu-id="c5303-214">Authors</span></span>  | <span data-ttu-id="c5303-215">System.Author</span><span class="sxs-lookup"><span data-stu-id="c5303-215">System.Author</span></span>        | <span data-ttu-id="c5303-216">1</span><span class="sxs-lookup"><span data-stu-id="c5303-216">1</span></span>        |
| <span data-ttu-id="c5303-217">Título</span><span class="sxs-lookup"><span data-stu-id="c5303-217">Title</span></span>    | <span data-ttu-id="c5303-218">System.Title</span><span class="sxs-lookup"><span data-stu-id="c5303-218">System.Title</span></span>         | <span data-ttu-id="c5303-219">1</span><span class="sxs-lookup"><span data-stu-id="c5303-219">1</span></span>        |
| <span data-ttu-id="c5303-220">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5303-220">Type</span></span>     | <span data-ttu-id="c5303-221">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="c5303-221">System.PerceivedType</span></span> | <span data-ttu-id="c5303-222">1</span><span class="sxs-lookup"><span data-stu-id="c5303-222">1</span></span>        |
| <span data-ttu-id="c5303-223">Categoria</span><span class="sxs-lookup"><span data-stu-id="c5303-223">Category</span></span> | <span data-ttu-id="c5303-224">System. Category</span><span class="sxs-lookup"><span data-stu-id="c5303-224">System.Category</span></span>      | <span data-ttu-id="c5303-225">2</span><span class="sxs-lookup"><span data-stu-id="c5303-225">2</span></span>        |
| <span data-ttu-id="c5303-226">Marcas</span><span class="sxs-lookup"><span data-stu-id="c5303-226">Tags</span></span>     | <span data-ttu-id="c5303-227">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="c5303-227">System.Keywords</span></span>      | <span data-ttu-id="c5303-228">2</span><span class="sxs-lookup"><span data-stu-id="c5303-228">2</span></span>        |



 

## <a name="music"></a><span data-ttu-id="c5303-229">Música</span><span class="sxs-lookup"><span data-stu-id="c5303-229">Music</span></span>



| <span data-ttu-id="c5303-230">Nome</span><span class="sxs-lookup"><span data-stu-id="c5303-230">Name</span></span>         | <span data-ttu-id="c5303-231">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c5303-231">Property</span></span>                     | <span data-ttu-id="c5303-232">Prioridade</span><span class="sxs-lookup"><span data-stu-id="c5303-232">Priority</span></span> |
|--------------|------------------------------|----------|
| \#           | <span data-ttu-id="c5303-233">System. Music. TrackNumber</span><span class="sxs-lookup"><span data-stu-id="c5303-233">System.Music.TrackNumber</span></span>     | <span data-ttu-id="c5303-234">1</span><span class="sxs-lookup"><span data-stu-id="c5303-234">1</span></span>        |
| <span data-ttu-id="c5303-235">Álbuns</span><span class="sxs-lookup"><span data-stu-id="c5303-235">Album</span></span>        | <span data-ttu-id="c5303-236">System. Music. campos AlbumTitle</span><span class="sxs-lookup"><span data-stu-id="c5303-236">System.Music.AlbumTitle</span></span>      | <span data-ttu-id="c5303-237">1</span><span class="sxs-lookup"><span data-stu-id="c5303-237">1</span></span>        |
| <span data-ttu-id="c5303-238">Artistas</span><span class="sxs-lookup"><span data-stu-id="c5303-238">Artists</span></span>      | <span data-ttu-id="c5303-239">System. Music. artista</span><span class="sxs-lookup"><span data-stu-id="c5303-239">System.Music.Artist</span></span>          | <span data-ttu-id="c5303-240">1</span><span class="sxs-lookup"><span data-stu-id="c5303-240">1</span></span>        |
| <span data-ttu-id="c5303-241">Gênero</span><span class="sxs-lookup"><span data-stu-id="c5303-241">Genre</span></span>        | <span data-ttu-id="c5303-242">System. Music. Gênero</span><span class="sxs-lookup"><span data-stu-id="c5303-242">System.Music.Genre</span></span>           | <span data-ttu-id="c5303-243">1</span><span class="sxs-lookup"><span data-stu-id="c5303-243">1</span></span>        |
| <span data-ttu-id="c5303-244">Classificação</span><span class="sxs-lookup"><span data-stu-id="c5303-244">Rating</span></span>       | <span data-ttu-id="c5303-245">System. rating</span><span class="sxs-lookup"><span data-stu-id="c5303-245">System.Rating</span></span>                | <span data-ttu-id="c5303-246">1</span><span class="sxs-lookup"><span data-stu-id="c5303-246">1</span></span>        |
| <span data-ttu-id="c5303-247">Título</span><span class="sxs-lookup"><span data-stu-id="c5303-247">Title</span></span>        | <span data-ttu-id="c5303-248">System.Title</span><span class="sxs-lookup"><span data-stu-id="c5303-248">System.Title</span></span>                 | <span data-ttu-id="c5303-249">1</span><span class="sxs-lookup"><span data-stu-id="c5303-249">1</span></span>        |
| <span data-ttu-id="c5303-250">Artista do álbum</span><span class="sxs-lookup"><span data-stu-id="c5303-250">Album Artist</span></span> | <span data-ttu-id="c5303-251">System. Music. AlbumArtist</span><span class="sxs-lookup"><span data-stu-id="c5303-251">System.Music.AlbumArtist</span></span>     | <span data-ttu-id="c5303-252">2</span><span class="sxs-lookup"><span data-stu-id="c5303-252">2</span></span>        |
| <span data-ttu-id="c5303-253">Taxa de bits</span><span class="sxs-lookup"><span data-stu-id="c5303-253">Bit Rate</span></span>     | <span data-ttu-id="c5303-254">System. Audio. EncodingBitrate</span><span class="sxs-lookup"><span data-stu-id="c5303-254">System.Audio.EncodingBitrate</span></span> | <span data-ttu-id="c5303-255">2</span><span class="sxs-lookup"><span data-stu-id="c5303-255">2</span></span>        |
| <span data-ttu-id="c5303-256">Condutores</span><span class="sxs-lookup"><span data-stu-id="c5303-256">Conductors</span></span>   | <span data-ttu-id="c5303-257">Sistema. Music. condutor</span><span class="sxs-lookup"><span data-stu-id="c5303-257">System.Music.Conductor</span></span>       | <span data-ttu-id="c5303-258">2</span><span class="sxs-lookup"><span data-stu-id="c5303-258">2</span></span>        |
| <span data-ttu-id="c5303-259">Comprimento</span><span class="sxs-lookup"><span data-stu-id="c5303-259">Length</span></span>       | <span data-ttu-id="c5303-260">System. Media. Duration</span><span class="sxs-lookup"><span data-stu-id="c5303-260">System.Media.Duration</span></span>        | <span data-ttu-id="c5303-261">2</span><span class="sxs-lookup"><span data-stu-id="c5303-261">2</span></span>        |
| <span data-ttu-id="c5303-262">Protegido</span><span class="sxs-lookup"><span data-stu-id="c5303-262">Protected</span></span>    | <span data-ttu-id="c5303-263">System. DRM. isproteged</span><span class="sxs-lookup"><span data-stu-id="c5303-263">System.DRM.IsProtected</span></span>       | <span data-ttu-id="c5303-264">2</span><span class="sxs-lookup"><span data-stu-id="c5303-264">2</span></span>        |
| <span data-ttu-id="c5303-265">Year</span><span class="sxs-lookup"><span data-stu-id="c5303-265">Year</span></span>         | <span data-ttu-id="c5303-266">Sistema. Media. Year</span><span class="sxs-lookup"><span data-stu-id="c5303-266">System.Media.Year</span></span>            | <span data-ttu-id="c5303-267">2</span><span class="sxs-lookup"><span data-stu-id="c5303-267">2</span></span>        |



 

## <a name="pictures"></a><span data-ttu-id="c5303-268">Imagens</span><span class="sxs-lookup"><span data-stu-id="c5303-268">Pictures</span></span>



| <span data-ttu-id="c5303-269">Nome</span><span class="sxs-lookup"><span data-stu-id="c5303-269">Name</span></span>          | <span data-ttu-id="c5303-270">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c5303-270">Property</span></span>                        | <span data-ttu-id="c5303-271">Prioridade</span><span class="sxs-lookup"><span data-stu-id="c5303-271">Priority</span></span> |
|---------------|---------------------------------|----------|
| <span data-ttu-id="c5303-272">Data de importação</span><span class="sxs-lookup"><span data-stu-id="c5303-272">Date imported</span></span> | <span data-ttu-id="c5303-273">System. DateImported</span><span class="sxs-lookup"><span data-stu-id="c5303-273">System.DateImported</span></span>             | <span data-ttu-id="c5303-274">1</span><span class="sxs-lookup"><span data-stu-id="c5303-274">1</span></span>        |
| <span data-ttu-id="c5303-275">Data de início</span><span class="sxs-lookup"><span data-stu-id="c5303-275">Date Taken</span></span>    | <span data-ttu-id="c5303-276">System. Photo. DateTaken</span><span class="sxs-lookup"><span data-stu-id="c5303-276">System.Photo.DateTaken</span></span>          | <span data-ttu-id="c5303-277">1</span><span class="sxs-lookup"><span data-stu-id="c5303-277">1</span></span>        |
| <span data-ttu-id="c5303-278">Classificação</span><span class="sxs-lookup"><span data-stu-id="c5303-278">Rating</span></span>        | <span data-ttu-id="c5303-279">System. rating</span><span class="sxs-lookup"><span data-stu-id="c5303-279">System.Rating</span></span>                   | <span data-ttu-id="c5303-280">1</span><span class="sxs-lookup"><span data-stu-id="c5303-280">1</span></span>        |
| <span data-ttu-id="c5303-281">Marcas</span><span class="sxs-lookup"><span data-stu-id="c5303-281">Tags</span></span>          | <span data-ttu-id="c5303-282">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="c5303-282">System.Keywords</span></span>                 | <span data-ttu-id="c5303-283">1</span><span class="sxs-lookup"><span data-stu-id="c5303-283">1</span></span>        |
| <span data-ttu-id="c5303-284">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5303-284">Type</span></span>          | <span data-ttu-id="c5303-285">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="c5303-285">System.PerceivedType</span></span>            | <span data-ttu-id="c5303-286">1</span><span class="sxs-lookup"><span data-stu-id="c5303-286">1</span></span>        |
| <span data-ttu-id="c5303-287">Autores</span><span class="sxs-lookup"><span data-stu-id="c5303-287">Authors</span></span>       | <span data-ttu-id="c5303-288">System.Author</span><span class="sxs-lookup"><span data-stu-id="c5303-288">System.Author</span></span>                   | <span data-ttu-id="c5303-289">2</span><span class="sxs-lookup"><span data-stu-id="c5303-289">2</span></span>        |
| <span data-ttu-id="c5303-290">Criador de câmera</span><span class="sxs-lookup"><span data-stu-id="c5303-290">Camera maker</span></span>  | <span data-ttu-id="c5303-291">System. Photo. CameraManufacturer</span><span class="sxs-lookup"><span data-stu-id="c5303-291">System.Photo.CameraManufacturer</span></span> | <span data-ttu-id="c5303-292">2</span><span class="sxs-lookup"><span data-stu-id="c5303-292">2</span></span>        |
| <span data-ttu-id="c5303-293">Modelo de câmera</span><span class="sxs-lookup"><span data-stu-id="c5303-293">Camera model</span></span>  | <span data-ttu-id="c5303-294">System. Photo. CameraModel</span><span class="sxs-lookup"><span data-stu-id="c5303-294">System.Photo.CameraModel</span></span>        | <span data-ttu-id="c5303-295">2</span><span class="sxs-lookup"><span data-stu-id="c5303-295">2</span></span>        |
| <span data-ttu-id="c5303-296">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5303-296">Comments</span></span>      | <span data-ttu-id="c5303-297">Sistema. Comment</span><span class="sxs-lookup"><span data-stu-id="c5303-297">System.Comment</span></span>                  | <span data-ttu-id="c5303-298">2</span><span class="sxs-lookup"><span data-stu-id="c5303-298">2</span></span>        |
| <span data-ttu-id="c5303-299">Dimensões</span><span class="sxs-lookup"><span data-stu-id="c5303-299">Dimensions</span></span>    | <span data-ttu-id="c5303-300">System. Image. Dimensions</span><span class="sxs-lookup"><span data-stu-id="c5303-300">System.Image.Dimensions</span></span>         | <span data-ttu-id="c5303-301">2</span><span class="sxs-lookup"><span data-stu-id="c5303-301">2</span></span>        |



 

## <a name="videos"></a><span data-ttu-id="c5303-302">Vídeos</span><span class="sxs-lookup"><span data-stu-id="c5303-302">Videos</span></span>



| <span data-ttu-id="c5303-303">Nome</span><span class="sxs-lookup"><span data-stu-id="c5303-303">Name</span></span>         | <span data-ttu-id="c5303-304">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c5303-304">Property</span></span>                 | <span data-ttu-id="c5303-305">Prioridade</span><span class="sxs-lookup"><span data-stu-id="c5303-305">Priority</span></span> |
|--------------|--------------------------|----------|
| <span data-ttu-id="c5303-306">Comprimento</span><span class="sxs-lookup"><span data-stu-id="c5303-306">Length</span></span>       | <span data-ttu-id="c5303-307">System. Media. Duration</span><span class="sxs-lookup"><span data-stu-id="c5303-307">System.Media.Duration</span></span>    | <span data-ttu-id="c5303-308">1</span><span class="sxs-lookup"><span data-stu-id="c5303-308">1</span></span>        |
| <span data-ttu-id="c5303-309">Classificação</span><span class="sxs-lookup"><span data-stu-id="c5303-309">Rating</span></span>       | <span data-ttu-id="c5303-310">System. rating</span><span class="sxs-lookup"><span data-stu-id="c5303-310">System.Rating</span></span>            | <span data-ttu-id="c5303-311">1</span><span class="sxs-lookup"><span data-stu-id="c5303-311">1</span></span>        |
| <span data-ttu-id="c5303-312">Marcas</span><span class="sxs-lookup"><span data-stu-id="c5303-312">Tags</span></span>         | <span data-ttu-id="c5303-313">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="c5303-313">System.Keywords</span></span>          | <span data-ttu-id="c5303-314">1</span><span class="sxs-lookup"><span data-stu-id="c5303-314">1</span></span>        |
| <span data-ttu-id="c5303-315">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5303-315">Type</span></span>         | <span data-ttu-id="c5303-316">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="c5303-316">System.PerceivedType</span></span>     | <span data-ttu-id="c5303-317">1</span><span class="sxs-lookup"><span data-stu-id="c5303-317">1</span></span>        |
| <span data-ttu-id="c5303-318">Altura do quadro</span><span class="sxs-lookup"><span data-stu-id="c5303-318">Frame height</span></span> | <span data-ttu-id="c5303-319">System. vídeo. FrameHeight</span><span class="sxs-lookup"><span data-stu-id="c5303-319">System.Video.FrameHeight</span></span> | <span data-ttu-id="c5303-320">2</span><span class="sxs-lookup"><span data-stu-id="c5303-320">2</span></span>        |
| <span data-ttu-id="c5303-321">Largura do quadro</span><span class="sxs-lookup"><span data-stu-id="c5303-321">Frame width</span></span>  | <span data-ttu-id="c5303-322">System. vídeo. FrameWidth</span><span class="sxs-lookup"><span data-stu-id="c5303-322">System.Video.FrameWidth</span></span>  | <span data-ttu-id="c5303-323">2</span><span class="sxs-lookup"><span data-stu-id="c5303-323">2</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c5303-324">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c5303-324">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c5303-325">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="c5303-325">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c5303-326">Desenvolvendo manipuladores de propriedade para o Windows Search</span><span class="sxs-lookup"><span data-stu-id="c5303-326">Developing Property Handlers for Windows Search</span></span>](-search-3x-wds-extidx-propertyhandlers.md)
</dt> <dt>

<span data-ttu-id="c5303-327">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="c5303-327">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c5303-328">Sistema de propriedades</span><span class="sxs-lookup"><span data-stu-id="c5303-328">Property System</span></span>](../properties/building-property-handlers.md)
</dt> <dt>

<span data-ttu-id="c5303-329">[Propriedades do sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="c5303-329">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> </dl>

 

 
