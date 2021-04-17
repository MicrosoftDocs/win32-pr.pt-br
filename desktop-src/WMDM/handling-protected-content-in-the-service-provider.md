---
title: Manipulando conteúdo protegido no provedor de serviços
description: Manipulando conteúdo protegido no provedor de serviços
ms.assetid: 5c18c8ec-d579-41df-8c25-c143fb9cdbef
keywords:
- Gerenciador de Dispositivos de mídia do Windows, certificados
- Gerenciador de Dispositivos, certificados
- Guia de programação, certificados
- provedores de serviços, certificados
- criando provedores de serviços, certificados
- certificates
- Windows Media Gerenciador de Dispositivos, conteúdo protegido por DRM
- Gerenciador de Dispositivos, conteúdo protegido por DRM
- Guia de programação, conteúdo protegido por DRM
- provedores de serviços, conteúdo protegido por DRM
- criando provedores de serviços, conteúdo protegido por DRM
- Conteúdo protegido por DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d10cf9078cf9aaf631b65de968f01491a97781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105770536"
---
# <a name="handling-protected-content-in-the-service-provider"></a>Manipulando conteúdo protegido no provedor de serviços

Você pode criar um provedor de serviços que possa enviar conteúdo protegido por DRM para um dispositivo criado em DRM (PDDRM) de dispositivo portátil, mas não é possível criar um provedor de serviços que possa enviar conteúdo protegido por DRM para dispositivos criados no Windows Media DRM 10 para dispositivos portáteis. Esses dispositivos usam MTP e você não pode criar seu próprio provedor de serviços do MTP.

A única etapa extra que um provedor de serviços deve executar para enviar material DRM para um dispositivo PDDRM é obter um par certificado/chave emitido pela Microsoft. Consulte [ferramentas para desenvolvimento](tools-for-development.md) para saber onde obter esse certificado/chave. As licenças emitidas para esses dispositivos serão licenças simplificadas que oferecem suporte apenas à reprodução simples de conteúdo comprado; Eles não oferecerão suporte a licenças de expiração de tempo. Essa licença será criada para você pelo provedor de conteúdo seguro (fornecido pela Microsoft para arquivos WMA/WMV) e armazenada no cabeçalho do arquivo enviado para o provedor de serviços. Você não precisará executar nenhuma etapa especial para arquivos protegidos.

Depois de enviar o arquivo protegido, o Windows Media Gerenciador de Dispositivos chamará o provedor de serviços para solicitar um arquivo de armazenamento de licença especial do dispositivo. O Windows Media Gerenciador de Dispositivos adicionará uma cópia da nova licença a esse arquivo e a retornará ao provedor de serviços para enviar de volta para o dispositivo. No entanto, mesmo que o provedor de serviços não consiga localizar ou retornar esse arquivo, o dispositivo ainda deve ser capaz de reproduzir o arquivo protegido usando a cópia de licença no cabeçalho do arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um provedor de serviços**](creating-a-service-provider.md)
</dt> <dt>

[**Lidando com conteúdo protegido**](handling-protected-content.md)
</dt> </dl>

 

 




