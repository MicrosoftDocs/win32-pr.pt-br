---
title: Usando o modelo de evento Media Foundation
description: Usando o modelo de evento Media Foundation
ms.assetid: c07425dc-25d0-430b-a1f6-6373303a0cc7
keywords:
- SDK de formato de mídia do Windows, modelo de evento de Media Foundation DRM
- SDK do Windows Media Format, Media Foundation modelo de eventos
- SDK do Windows Media Format, modelo de evento do DRM
- DRM (gerenciamento de direitos digitais), Media Foundation modelo de eventos
- DRM (gerenciamento de direitos digitais), Media Foundation modelo de eventos
- DRM (gerenciamento de direitos digitais), modelo de evento
- DRM (gerenciamento de direitos digitais), modelo de evento
- DRM (gerenciamento de direitos digitais), interface IWMDRMEventGenerator
- DRM (gerenciamento de direitos digitais), interface IWMDRMEventGenerator
- Media Foundation
- IWMDRMEventGenerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58d48157072cf8814ff8ac74d97a965f9e772e3
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104007182"
---
# <a name="using-the-media-foundation-event-model"></a>Usando o modelo de evento Media Foundation

Os métodos assíncronos com suporte das APIs estendidas do cliente DRM do Windows Media usam o mesmo modelo de evento usado pelo SDK do Media Foundation. Cada objeto que dá suporte a métodos assíncronos implementa a interface [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md) , que pode ser usada para recuperar um evento quando uma operação assíncrona for concluída.

A interface **IWMDRMEventGenerator** herda da interface **IMFMediaEventGenerator** , que está documentada na documentação do SDK do Media Foundation.

O código de exemplo no [exemplo de individualização de DRM](drm-individualization-example.md) usa o método **IMFMediaEventGenerator:: GetEvent** para recuperar eventos da fila, um de cada vez. Usar **GetEvent** é mais simples do que usar **IMFMediaEventGenerator:: BeginGetEvent** e **IMFMediaEventGenerator:: EndGetEvent** com um retorno de chamada, o que torna os exemplos de código mais fáceis de entender. Se você usar **GetEvent** em seu código ou implementar **IMFAsyncCallback** e usar **BeginGetEvent** e **EndGetEvent**, a lógica para manipular o evento depois que ele foi recebido é a mesma.

Vários métodos assíncronos geram eventos que contêm referências a objetos que podem ser usados para obter informações de status mais detalhadas. Nesses casos, o evento gerado tem um ponteiro **IUnknown** como seu valor, que pode ser consultado para recuperar a interface de status. A lista a seguir resume as relações entre chamadas assíncronas, eventos gerados e outras interfaces.

-   O método [**IWMDRMLicenseManagement:: BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) gera eventos **MEWMDRMLicenseBackupProgress** com interfaces [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) associadas.
-   O método [**IWMDRMLicenseManagement:: RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md) gera eventos **MEWMDRMLicenseRestoreProgress** com interfaces [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) associadas.
-   O método [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) , quando usado para executar a individualização, gera eventos **MEWMDRMIndividualizationProgress** com interfaces [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) associadas.
-   O método [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) , quando usado para preparar dados para aquisição de licença não silenciosa, gera um evento **MEWMDRMLicenseAcquisitionCompleted** com uma interface [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) associada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exemplo de individualização de DRM**](drm-individualization-example.md)
</dt> <dt>

[**Introdução**](drm-getting-started.md)
</dt> <dt>

[Documentação do SDK do Media Foundation](https://www.microsoft.com/?ref=go)
</dt> </dl>

 

 




