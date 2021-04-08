---
description: A seguir estão as funções de ImageHlp.
ms.assetid: 926f412e-25ba-4f9c-a118-b5a1bc723379
title: Funções do ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e921707474f68e288f67e84dda9e361922bca0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920484"
---
# <a name="imagehlp-functions"></a>Funções do ImageHlp

A seguir estão as funções de ImageHlp.

## <a name="image-access"></a>Acesso à imagem

As funções de acesso à imagem acessam os dados em uma imagem executável. As funções fornecem acesso de alto nível à base de imagens e acesso muito específico às partes mais comuns dos dados de uma imagem.

<dl>

[**GetImageConfigInformation**](/windows/desktop/api/Imagehlp/nf-imagehlp-getimageconfiginformation)  
[**GetImageUnusedHeaderBytes**](/windows/desktop/api/Imagehlp/nf-imagehlp-getimageunusedheaderbytes)  
[**ImageLoad**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageload)  
[**ImageUnload**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageunload)  
[**MapAndLoad**](/windows/desktop/api/Imagehlp/nf-imagehlp-mapandload)  
[**SetImageConfigInformation**](/windows/desktop/api/Imagehlp/nf-imagehlp-setimageconfiginformation)  
[**UnMapAndLoad**](/windows/desktop/api/Imagehlp/nf-imagehlp-unmapandload)  
</dl>

## <a name="image-integrity"></a>Integridade da imagem

As funções de integridade da imagem gerenciam o conjunto de certificados em um arquivo de imagem.

<dl>

[**DigestFunction**](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)  
[**ImageAddCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)  
[**ImageEnumerateCertificates**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)  
[**ImageGetCertificateData**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)  
[**ImageGetCertificateHeader**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)  
[**ImageGetDigestStream**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)  
[**ImageRemoveCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)  
</dl>

## <a name="image-modification"></a>Modificação de imagem

As funções de modificação de imagem permitem que você altere a imagem executável.

<dl>

[**BindImage**](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimage)  
[**BindImageEx**](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimageex)  
[**CheckSumMappedFile**](/windows/desktop/api/Imagehlp/nf-imagehlp-checksummappedfile)  
[**MapFileAndCheckSum**](/windows/desktop/api/Imagehlp/nf-imagehlp-mapfileandchecksuma)  
[**ReBaseImage**](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage)  
[**ReBaseImage64**](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage64)  
[**SplitSymbols**](/windows/desktop/api/Imagehlp/nf-imagehlp-splitsymbols)  
[**StatusRoutine**](/windows/desktop/api/Imagehlp/nc-imagehlp-pimagehlp_status_routine)  
[**TouchFileTimes**](/windows/desktop/api/Imagehlp/nf-imagehlp-touchfiletimes)  
[**UpdateDebugInfoFile**](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofile)  
[**UpdateDebugInfoFileEx**](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofileex)  
</dl>

 

 



