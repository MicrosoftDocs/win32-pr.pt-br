---
title: Fazendo backup e restaurando licenças DRM
description: Fazendo backup e restaurando licenças DRM
ms.assetid: ec2777e9-76af-43fe-8bd5-4d7532d2fb32
keywords:
- SDK do Windows Media Format, fazendo backup de licenças DRM
- SDK do Windows Media Format, restaurando licenças DRM
- SDK do Windows Media Format, licenças DRM
- SDK do Windows Media Format, licenças para DRM
- SDK do Windows Media Format, recurso de restauração de backup
- SDK do Windows Media Format, serviço de gerenciamento de licenças
- SDK do Windows Media Format, detecção de fraudes
- DRM (gerenciamento de direitos digitais), fazendo backup de licenças
- DRM (gerenciamento de direitos digitais), fazendo backup de licenças
- DRM (gerenciamento de direitos digitais), restaurando licenças
- DRM (gerenciamento de direitos digitais), restaurando licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), recurso de restauração de backup
- DRM (gerenciamento de direitos digitais), recurso de restauração de backup
- DRM (gerenciamento de direitos digitais), serviço de gerenciamento de licenças
- DRM (gerenciamento de direitos digitais), serviço de gerenciamento de licenças
- DRM (gerenciamento de direitos digitais), detecção de fraudes
- DRM (gerenciamento de direitos digitais), detecção de fraudes
- fazendo backup de licenças DRM
- restaurando licenças DRM
- licenças, DRM
- licenças, fazendo backup de DRM
- licenças, restaurando DRM
- Recurso de restauração de backup
- Serviço de gerenciamento de licenças
- detecção de fraudes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7718f03170077f7db624f8a99b8262239a79ca9
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104294565"
---
# <a name="backing-up-and-restoring-of-drm-licenses"></a><span data-ttu-id="32ee1-130">Fazendo backup e restaurando licenças DRM</span><span class="sxs-lookup"><span data-stu-id="32ee1-130">Backing Up and Restoring of DRM Licenses</span></span>

<span data-ttu-id="32ee1-131">Com o recurso de restauração de backup, os usuários podem fazer backup e restaurar [*licenças*](wmformat-glossary.md) no mesmo computador ou em outros computadores.</span><span class="sxs-lookup"><span data-stu-id="32ee1-131">With the Backup Restore feature, users can back up and restore [*licenses*](wmformat-glossary.md) to the same computer or to other computers.</span></span> <span data-ttu-id="32ee1-132">Esse recurso permite que os usuários transfiram licenças para um novo computador ou de volta para o mesmo computador (depois de reformatar o disco rígido, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="32ee1-132">This feature enables users to transfer licenses to a new computer or back to the same computer (after reformatting the hard disk, for example).</span></span> <span data-ttu-id="32ee1-133">Além disso, os usuários podem reproduzir arquivos ASF protegidos em mais de um computador.</span><span class="sxs-lookup"><span data-stu-id="32ee1-133">In addition, users can play protected ASF files on more than one computer.</span></span>

<span data-ttu-id="32ee1-134">Para incentivar o uso legítimo de uma licença, uma política de detecção de fraude restringe o número de vezes que uma licença pode ser restaurada.</span><span class="sxs-lookup"><span data-stu-id="32ee1-134">To encourage legitimate use of a license, a fraud detection policy restricts the number of times a license can be restored.</span></span> <span data-ttu-id="32ee1-135">A Microsoft fornece um serviço que controla o número de computadores para os quais uma licença foi restaurada; se um limite for atingido, o usuário não poderá restaurar a licença.</span><span class="sxs-lookup"><span data-stu-id="32ee1-135">Microsoft provides a service that tracks the number of computers to which a license has been restored; if a limit is reached, the user cannot restore the license.</span></span>

## <a name="allowing-or-disallowing-the-right-to-back-up-and-restore"></a><span data-ttu-id="32ee1-136">Permitir ou não permitir o direito de fazer backup e restaurar</span><span class="sxs-lookup"><span data-stu-id="32ee1-136">Allowing or Disallowing the Right to Back Up and Restore</span></span>

<span data-ttu-id="32ee1-137">O recurso de restauração de backup funciona apenas para licenças para as quais o direito de backup e restauração é fornecido.</span><span class="sxs-lookup"><span data-stu-id="32ee1-137">The Backup Restore feature works only for licenses for which the Backup and Restore right is given.</span></span> <span data-ttu-id="32ee1-138">Se os proprietários de conteúdo ou os emissores de licença não quiserem esse recurso, ou se eles emitirem licenças que contenham um estado seguro (como operações contadas ou tempo limitado), eles poderão não permitir esse direito.</span><span class="sxs-lookup"><span data-stu-id="32ee1-138">If content owners or license issuers do not want this feature, or if they issue licenses that contain a secure state (such as counted operations or limited time), they can disallow this right.</span></span>

<span data-ttu-id="32ee1-139">Quando uma licença não pode ser restaurada porque um usuário não tem o direito, uma [*ID de chave*](wmformat-glossary.md) é passada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="32ee1-139">When a license cannot be restored because a user does not have the right, a [*key ID*](wmformat-glossary.md) is passed to the application.</span></span> <span data-ttu-id="32ee1-140">No mínimo, o usuário deve ser notificado de que não foi possível fazer o backup de algumas licenças, embora o usuário não saiba a quais licenças essa mensagem se refere.</span><span class="sxs-lookup"><span data-stu-id="32ee1-140">At a minimum, the user should be notified that some licenses could not be backed up, although the user does not know which licenses this message refers to.</span></span> <span data-ttu-id="32ee1-141">Se você souber a ID da chave para arquivos protegidos disponíveis, poderá desenvolver uma solução mais robusta para informar o usuário.</span><span class="sxs-lookup"><span data-stu-id="32ee1-141">If you know the key ID for available protected files, you can develop a more robust solution for informing the user.</span></span>

<span data-ttu-id="32ee1-142">Por exemplo, um player poderia ser desenvolvido para um rótulo de registro que fornece músicas protegidas na Internet.</span><span class="sxs-lookup"><span data-stu-id="32ee1-142">For example, a player could be developed for a record label that provides protected songs on the Internet.</span></span> <span data-ttu-id="32ee1-143">Essas músicas e suas IDs de chave podem ser rastreadas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="32ee1-143">These songs and their key IDs could be tracked in a database.</span></span> <span data-ttu-id="32ee1-144">Se não for possível fazer backup de algumas licenças, o aplicativo de Player poderá usar a ID de chave para consultar o banco de dados para o nome das músicas e informar ao usuário para quais músicas não é possível fazer backup das licenças.</span><span class="sxs-lookup"><span data-stu-id="32ee1-144">If some licenses could not be backed up, the player application could use the key ID to query the database for the name of the songs, then inform the user for which songs the licenses cannot be backed up.</span></span> <span data-ttu-id="32ee1-145">Ou, uma biblioteca de música pode ser criada para cada usuário localmente e a ID da chave pode ser usada para recuperar mais informações sobre quais licenças não puderam ser submetidas a backup.</span><span class="sxs-lookup"><span data-stu-id="32ee1-145">Or, a music library could be created for each user locally, and the key ID could be used to retrieve more information about which licenses could not be backed up.</span></span>

## <a name="the-license-management-service"></a><span data-ttu-id="32ee1-146">O serviço de gerenciamento de licenças</span><span class="sxs-lookup"><span data-stu-id="32ee1-146">The License Management Service</span></span>

<span data-ttu-id="32ee1-147">Quando o recurso de restauração de backup é implementado, um serviço de gerenciamento de licenças hospedado pela Microsoft gerencia a restauração de licenças.</span><span class="sxs-lookup"><span data-stu-id="32ee1-147">When the Backup Restore feature is implemented, a License Management Service that is hosted by Microsoft manages the restoration of licenses.</span></span>

<span data-ttu-id="32ee1-148">Primeiro, os usuários fazem backup de licenças no aplicativo, por exemplo, escolhendo uma opção de menu.</span><span class="sxs-lookup"><span data-stu-id="32ee1-148">First, users back up licenses in the application, for example, by choosing a menu option.</span></span> <span data-ttu-id="32ee1-149">Todas as licenças no computador são submetidas a backup em um local especificado, como um disquete.</span><span class="sxs-lookup"><span data-stu-id="32ee1-149">All licenses on the computer are backed up to a specified location, such as a floppy disk.</span></span> <span data-ttu-id="32ee1-150">Em seguida, os usuários restauram licenças usando o aplicativo, por exemplo, escolhendo uma opção de menu e especificando seu local de backup.</span><span class="sxs-lookup"><span data-stu-id="32ee1-150">Then, users restore licenses by using the application, for example, by choosing a menu option and specifying their backup location.</span></span>

<span data-ttu-id="32ee1-151">Neste ponto, o usuário deve estar conectado à Internet; uma solicitação do aplicativo é enviada para o serviço de gerenciamento de licenças.</span><span class="sxs-lookup"><span data-stu-id="32ee1-151">At this point, the user must be connected to the Internet; a request from the application is sent to the License Management Service.</span></span> <span data-ttu-id="32ee1-152">Se o computador do qual foi feito o backup da licença for diferente do computador original (ou se o computador original tiver sido reformatado), o serviço de gerenciamento de licenças emitirá uma nova licença para o novo computador.</span><span class="sxs-lookup"><span data-stu-id="32ee1-152">If the computer from which the license was backed up is different from the original computer (or the original computer has been reformatted), the License Management Service issues a new license to the new computer.</span></span> <span data-ttu-id="32ee1-153">Caso contrário, a licença que foi emitida anteriormente para esse computador será reemitida.</span><span class="sxs-lookup"><span data-stu-id="32ee1-153">Otherwise, the license that was previously issued to that computer is reissued.</span></span>

<span data-ttu-id="32ee1-154">Como o serviço de gerenciamento de licenças recupera informações do usuário, você deve exibir a política de privacidade da Microsoft ou fornecer um link para essa página no [site da Microsoft](https://www.microsoft.com/licensing/default).</span><span class="sxs-lookup"><span data-stu-id="32ee1-154">Because the License Management Service retrieves information from the user, you must display the Microsoft privacy policy or provide a link to that page at the [Microsoft Web site](https://www.microsoft.com/licensing/default).</span></span>

> [!Note]  
> <span data-ttu-id="32ee1-155">Quando um usuário final restaura uma licença para um computador diferente e a licença requer individualização, o usuário final deve autorizar os componentes DRM a serem atualizados.</span><span class="sxs-lookup"><span data-stu-id="32ee1-155">When an end user restores a license to a different computer and the license requires individualization, the end user must authorize the DRM components to be updated.</span></span> <span data-ttu-id="32ee1-156">Você deve implementar um processo em seu aplicativo de Player para dar suporte a esse recurso.</span><span class="sxs-lookup"><span data-stu-id="32ee1-156">You must implement a process in your player application to support this feature.</span></span>

 

## <a name="detecting-fraud"></a><span data-ttu-id="32ee1-157">Detectando fraude</span><span class="sxs-lookup"><span data-stu-id="32ee1-157">Detecting Fraud</span></span>

<span data-ttu-id="32ee1-158">O usuário tem permissão para restaurar uma licença por um número limitado de vezes.</span><span class="sxs-lookup"><span data-stu-id="32ee1-158">The user is allowed to restore a license a limited number of times.</span></span> <span data-ttu-id="32ee1-159">Cada vez que uma licença é restaurada, o serviço de gerenciamento de licenças a acompanha e incrementa a contagem dessa licença em uma.</span><span class="sxs-lookup"><span data-stu-id="32ee1-159">Each time a license is restored, the License Management Service tracks it and increments the count for that license by one.</span></span> <span data-ttu-id="32ee1-160">Ao restaurar uma licença para um computador no qual a licença foi restaurada anteriormente (por exemplo, o computador do qual foi feito o backup da licença), a contagem não é aumentada.</span><span class="sxs-lookup"><span data-stu-id="32ee1-160">When restoring a license to a computer to which the license has been restored previously (for example, the computer from which the license was backed up), the count is not increased.</span></span> <span data-ttu-id="32ee1-161">Um computador é considerado diferente se tiver um novo sistema operacional ou se o sistema operacional tiver sido reinstalado.</span><span class="sxs-lookup"><span data-stu-id="32ee1-161">A computer is considered to be different if it has a new operating system, or the operating system has been re-installed.</span></span>

<span data-ttu-id="32ee1-162">De acordo com a política de detecção de fraudes da Microsoft, quando uma licença é restaurada um determinado número de vezes, o aplicativo recebe uma URL dos componentes do DRM e é responsável por abrir um navegador e exibir a página da Web, o que indica que o contrato de licença pode ter sido violado.</span><span class="sxs-lookup"><span data-stu-id="32ee1-162">In accordance with Microsoft's fraud detection policy, when a license has been restored a certain number of times, the application receives a URL from the DRM components and is responsible for opening a browser and displaying the Web page, which indicates that the license agreement might have been violated.</span></span> <span data-ttu-id="32ee1-163">O usuário deve entrar em contato com o distribuidor de licenças, que deve determinar se a solicitação é válida.</span><span class="sxs-lookup"><span data-stu-id="32ee1-163">The user must contact the license distributor, who must then determine whether the request is valid.</span></span>

> [!Note]  
> <span data-ttu-id="32ee1-164">O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="32ee1-164">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="32ee1-165">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32ee1-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32ee1-166">**Recursos de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="32ee1-166">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="32ee1-167">**Fazendo backup e restaurando licenças**</span><span class="sxs-lookup"><span data-stu-id="32ee1-167">**Backing Up and Restoring Licenses**</span></span>](backing-up-and-restoring-licenses.md)
</dt> </dl>

 

 




