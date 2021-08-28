---
description: Conversão manual do MTS
ms.assetid: 7ecc64a8-783d-4238-8b63-8e9c76382723
title: Conversão manual do MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d384a6ca5f6afa2d0563249c78e1120349e28e053f1cad923a6ae2bdcdb8849
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070556"
---
# <a name="manual-conversion-from-mts"></a>Conversão manual do MTS

Talvez você queira isolar a conversão de pacotes MTS em aplicativos COM+ para que ela fique fora do processo Windows instalação. O procedimento a seguir oferece uma abordagem alternativa:

1.  Exporte os pacotes MTS usando o recurso Exportação de Pacotes MTS 2.0 (resultando em um arquivo de pacote MTS e uma coleção de outros arquivos).
2.  Exclua os pacotes MTS e atualize Windows ou execute uma instalação limpa do Windows.
3.  Instale os arquivos do pacote MTS (.ltd) em um sistema Windows 2000 ou posterior usando o assistente de Instalação de Aplicativos da ferramenta administrativa dos Serviços de Componentes. Você também precisará redefinir a identidade "Executar como" do aplicativo no registro do sistema em **HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ APPID \\ RunAs**.

> [!Note]  
> Somente o procedimento de conversão automática (por meio Windows ou executando o utilitário MTSTOCOM) gera o arquivo de log MTSTOCOM. Esse arquivo não é gerado ao seguir o procedimento de conversão manual.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conversão automática do MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Resultados e problemas de conversão COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Biblioteca de Administração do MTS](mts-administration-library.md)
</dt> </dl>

 

 



