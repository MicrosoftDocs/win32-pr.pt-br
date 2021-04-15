---
description: Localizando recursos não Win32 PE
ms.assetid: 12f0b78e-ca85-443a-94ea-6bec5aa40c06
title: Localizando recursos não Win32 PE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 079288cd6200eb64289f474636cbc8dc046c1e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760844"
---
# <a name="locating-non-win32-pe-resources"></a><span data-ttu-id="fc1ff-103">Localizando recursos não Win32 PE</span><span class="sxs-lookup"><span data-stu-id="fc1ff-103">Locating Non-Win32 PE Resources</span></span>

<span data-ttu-id="fc1ff-104">Para localizar recursos não Win32 PE, seu aplicativo deve primeiro chamar a função [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) para localizar o arquivo de recurso específico do idioma do qual os recursos devem ser carregados.</span><span class="sxs-lookup"><span data-stu-id="fc1ff-104">To locate non-Win32 PE resources, your application should first call the [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) function to locate the language-specific resource file from which to load resources.</span></span> <span data-ttu-id="fc1ff-105">Se o aplicativo estiver seguindo as configurações de idioma do sistema, ele deverá chamar a função com o \_ nome do idioma \_ do MUI \| \_ \_ \_ idiomas da interface do usuário preferencial do MUI \_ especificados para *dwFlags* e **null** especificados para *pwszLanguage*.</span><span class="sxs-lookup"><span data-stu-id="fc1ff-105">If the application is following system language settings, it must call the function with MUI\_LANGUAGE\_NAME \| MUI\_USER\_PREFERRED\_UI\_LANGUAGES specified for *dwFlags* and **NULL** specified for *pwszLanguage*.</span></span> <span data-ttu-id="fc1ff-106">Se o aplicativo estiver seguindo as configurações de idioma específicas do aplicativo, ele usará **GetFileMUIPath** para determinar se existe um arquivo específico de idioma especificando o idioma no parâmetro *pwszLanguage* .</span><span class="sxs-lookup"><span data-stu-id="fc1ff-106">If the application is following application-specific language settings, it uses **GetFileMUIPath** to determine if a language-specific file exists by specifying the language in the *pwszLanguage* parameter.</span></span>

<span data-ttu-id="fc1ff-107">Após a chamada para [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath), o aplicativo deve definir a funcionalidade personalizada para carregar o módulo de recurso e carregar recursos específicos dele.</span><span class="sxs-lookup"><span data-stu-id="fc1ff-107">After the call to [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath), the application must define custom functionality to load the resource module and load specific resources from it.</span></span> <span data-ttu-id="fc1ff-108">Por exemplo, se você estiver usando um arquivo de recurso. txt ou. xml, o aplicativo deverá usar um analisador TXT ou XML para carregar o arquivo e, em seguida, analisar o conteúdo do arquivo para cada recurso necessário.</span><span class="sxs-lookup"><span data-stu-id="fc1ff-108">For example, if you are using a .txt or .xml resource file, the application must use a TXT or XML parser to load the file and then parse the contents of the file for each required resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc1ff-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc1ff-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc1ff-110">Usando a interface do usuário multilíngue</span><span class="sxs-lookup"><span data-stu-id="fc1ff-110">Using Multilingual User Interface</span></span>](using-multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="fc1ff-111">**GetFileMUIPath**</span><span class="sxs-lookup"><span data-stu-id="fc1ff-111">**GetFileMUIPath**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)
</dt> </dl>

 

 



