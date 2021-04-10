---
description: Registrando codecs MPEG2
ms.assetid: f730a7df-af8f-4dce-9bfe-6ee1eca8fd90
title: Registrando codecs MPEG2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de007cebdd0a911f6b43f21003ed3ede0bc1723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087477"
---
# <a name="registering-mpeg2-codecs"></a><span data-ttu-id="0ad64-103">Registrando codecs MPEG2</span><span class="sxs-lookup"><span data-stu-id="0ad64-103">Registering MPEG2 Codecs</span></span>

<span data-ttu-id="0ad64-104">Este tópico aplica-se somente ao Windows XP Media Center Edition.</span><span class="sxs-lookup"><span data-stu-id="0ad64-104">This topic applies to Windows XP Media Center Edition only.</span></span>

<span data-ttu-id="0ad64-105">O Windows XP Media Center Edition mantém duas chaves do registro que ele usa para determinar qual codec usar para reproduzir arquivos de vídeo e áudio do MPEG2.</span><span class="sxs-lookup"><span data-stu-id="0ad64-105">Windows XP Media Center Edition maintains two registry keys that it uses to determine which codec to use to play back MPEG2 video and audio files.</span></span> <span data-ttu-id="0ad64-106">A primeira chave do Registro especifica o codec MPEG2 preferencial do fabricante do computador e a segunda lista todos os codecs compatíveis com o Media Center que estão atualmente instalados no computador.</span><span class="sxs-lookup"><span data-stu-id="0ad64-106">The first registry key specifies the computer manufacturer's preferred MPEG2 codec, and the second lists all of the Media Center compatible codecs that are currently installed on the computer.</span></span> <span data-ttu-id="0ad64-107">Quando o Media Center precisar reproduzir um arquivo MPEG2, ele usará o codec preferencial do fabricante, se um for especificado.</span><span class="sxs-lookup"><span data-stu-id="0ad64-107">When Media Center needs to play back an MPEG2 file, it uses the manufacturer's preferred codec, if one is specified.</span></span> <span data-ttu-id="0ad64-108">Caso contrário, ele usará o primeiro codec compatível com o Media Center listado no registro.</span><span class="sxs-lookup"><span data-stu-id="0ad64-108">If not, it uses the first Media Center compatible codec listed in the registry.</span></span> <span data-ttu-id="0ad64-109">Se o registro não especificar nenhum codec preferencial ou compatível, o Media Center usará o mérito de filtro padrão do DirectShow para escolher um codec.</span><span class="sxs-lookup"><span data-stu-id="0ad64-109">If the registry specifies no preferred or compatible codecs, Media Center uses the standard DirectShow filter merit to choose a codec.</span></span>

<span data-ttu-id="0ad64-110">Para garantir que o Media Center sempre use um codec MPEG2 compatível, os fabricantes de computadores do Media Center devem especificar o codec do MPEG2 preferencial no seguinte local do registro:</span><span class="sxs-lookup"><span data-stu-id="0ad64-110">To ensure that Media Center always uses a compatible MPEG2 codec, manufacturers of Media Center computers should specify the preferred MPEG2 codec at the following registry location:</span></span>


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Media Center\Service\Video
```



<span data-ttu-id="0ad64-111">Os dados de chave devem ser os seguintes:</span><span class="sxs-lookup"><span data-stu-id="0ad64-111">The key data should be as follows:</span></span>


```C++
PreferredMPEG2VideoDecoder=REG_SZ "{MPEG2 Video CLSID GUID}"
PreferredMPEG2AudioDecoder=REG_SZ "{MPEG2 Audio CLSID GUID}"
```



<span data-ttu-id="0ad64-112">O programa de instalação para um codec MPEG2 compatível com o Media Center deve registrar o codec criando duas instâncias da seguinte chave do registro — uma para o codec de vídeo e outra para o codec de áudio:</span><span class="sxs-lookup"><span data-stu-id="0ad64-112">The setup program for a Media Center compatible MPEG2 codec should register the codec by creating two instances of the following registry key—one for the video codec and one for the audio codec:</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\{083863F1-70DE-11d0-BD40-00A0C911CE86}\Instance\<Your Codec CLSID here>\Capabilities]
```



<span data-ttu-id="0ad64-113">Os dados de chave devem ser os seguintes:</span><span class="sxs-lookup"><span data-stu-id="0ad64-113">The key data should be as follows:</span></span>


```C++
"{374ac4df-7c98-4257-b13d-36087dbee458}"=dword:00000001
```



 

 



