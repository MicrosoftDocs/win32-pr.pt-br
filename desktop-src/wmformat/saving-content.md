---
title: Salvar conteúdo
description: Salvar conteúdo
ms.assetid: 22f4e580-43a4-48b5-8eb3-90e1346a1093
keywords:
- SDK do Windows Media Format, salvando conteúdo
- SDK do Windows Media Format, streaming de cache rápido
- ASF (Advanced Systems Format), salvando conteúdo
- ASF (formato de sistemas avançados), salvando conteúdo
- ASF (Advanced Systems Format), streaming de cache rápido
- ASF (formato de sistemas avançados), streaming de cache rápido
- fluxos, salvando conteúdo
- Streaming de cache rápido, salvando conteúdo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6c215a81accef29f8943ed52ca24264f785d94
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103640294"
---
# <a name="saving-content"></a>Salvar conteúdo

Ao usar esse SDK, um aplicativo pode salvar o conteúdo baixado ou transmitido no computador local do usuário, chamando o método [**IWMReaderAdvanced2:: SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) no objeto Reader. Para conteúdo transmitido, o servidor deve usar o streaming de cache rápido, que é descrito na seção [habilitando o streaming de cache rápido do cliente](enabling-fast-cache-streaming-from-the-client.md). Para conteúdo transmitido, o método **SaveFileAs** cria um arquivo ASX que aponta para um arquivo ASF que contém o conteúdo salvo. Se o objeto leitor estiver transmitindo uma lista de reprodução no servidor, cada entrada será salva como um arquivo ASF separado e o arquivo ASX apontará para cada um dos arquivos ASF. Para conteúdo baixado, o método **SaveFileAs** simplesmente cria um arquivo asf.

Para salvar o conteúdo em um arquivo local, faça o seguinte:

1.  Chame [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) com a URL. **Open** é uma chamada assíncrona e retorna imediatamente. Aguarde a conclusão da operação, conforme descrito em [para criar um leitor e abrir um arquivo](to-create-a-reader-and-open-a-file.md).
2.  Consulte o objeto de leitor para a interface [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) .
3.  Verifique se o conteúdo pode ser salvo chamando o método [**IWMReaderAdvanced4:: CanSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) . Se o método retornar false, o conteúdo não poderá ser salvo localmente. Caso contrário, vá para a etapa 4.
4.  Chame o método [**IWMReaderAdvanced4:: IsUsingFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) para determinar se o servidor está usando o streaming de cache rápido.
5.  Chame o [**IWMReaderAdvanced2:: SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) com um nome de arquivo para o arquivo local. Se o método **IsUsingFastCache** retornou true, dê ao nome do arquivo uma extensão. asx. Caso contrário, dê ao nome do arquivo uma extensão. ASF,. WMA ou. wmv.

O aplicativo pode cancelar a operação de salvamento enquanto está em andamento, chamando o método [**IWMReaderAdvanced4:: CancelSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) .

O conteúdo salvo pode ser protegido com DRM, portanto, talvez não seja possível reproduzir o arquivo em outro computador. Para obter mais informações sobre a proteção de conteúdo, consulte [recursos de Rights Management digital](digital-rights-management-features.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interface IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




