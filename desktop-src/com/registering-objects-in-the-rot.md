---
title: Registrando objetos no corrompidos
description: Registrando objetos no corrompidos
ms.assetid: f479c2d1-0c55-4281-8f15-2f957fa03b70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d77e7bc6fe8b0a4d5896bf33575df2f57fb0e583f78acd02653f6ccb014f34ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104807"
---
# <a name="registering-objects-in-the-rot"></a>Registrando objetos no corrompidos

Normalmente, quando um cliente solicita que um servidor crie uma instância de objeto, o servidor normalmente cria um moniker para o objeto e o registra na tabela de objetos em execução (corrompidos) por meio de uma chamada para [**IRunningObjectTable:: Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register).

Quando o servidor chama [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) para criar um moniker de arquivo a ser registrado no corrompidos, os servidores devem passar nomes de arquivos locais que são baseados em unidade, não no formato UNC. Isso garante que os dados de comparação de moniker gerados pela chamada de registro corrompidos correspondam ao que é usado ao fazer uma pesquisa corrompidos na parte de um cliente remoto. Isso ocorre porque quando o serviço COM distribuído recebe uma solicitação de ativação de um arquivo local para o servidor de um cliente remoto, o arquivo é convertido em um caminho baseado em unidade local.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instalando como um aplicativo de serviço](installing-as-a-service-application.md)
</dt> <dt>

[Registrando uma classe na instalação](registering-a-class-at-installation.md)
</dt> <dt>

[Registrando um servidor EXE em execução](registering-a-running-exe-server.md)
</dt> <dt>

[Registro automático](self-registration.md)
</dt> </dl>

 

 




