---
description: Este tópico descreve como criar um especialista genérico que acompanha o SDK do Monitor de Rede.
ms.assetid: c05b261d-3fac-40bf-b4ff-bd766f8d148f
title: Criando um especialista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbffc036f27ad0b91fb19906c5f12740919828b33ebfced584e068abe93bd912
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064246"
---
# <a name="building-an-expert"></a>Criando um especialista

Este tópico descreve como criar um especialista genérico que acompanha o SDK do Monitor de Rede.

> [!Note]  
> Antes de criar os exemplos de código a seguir, instale o SDK do Monitor de Rede e inicialize o MySetEnv.bat arquivo.

 

**Para criar um especialista genérico**

1.  Abra um prompt Monitor de Rede comando e navegue até o subdiretório Especialistas; por exemplo, C: Arquivos de Programas \\ \\ Especialistas em \\ NetMonSDK2. \\
2.  Digite **xcopy /e /s /v Blrplate MyExpert**; em seguida, quando solicitado, digite **D.**
3.  Mova para o \\ subdiretório MyExpert.
4.  Digite **ren Blrplate. \* \* MyExpert \* \* .** Verifique se todos os arquivos foram renomeados corretamente. Verifique os nomes de arquivo comparando os arquivos no \\ subdiretório Experts \\ Blrplate.
5.  Edite o Makefile substituindo todas as ocorrências **de Blrplate** por **MyExpert.**
6.  Edite ambos os arquivos .cpp substituindo todas as ocorrências **de Blrplate** por **MyExpert.** Esteja ciente de que o identificador da caixa de diálogo em Config.cpp deve estar em maiúsculas (por exemplo, **MYEXPERT**).
7.  Edite MyExpert.h substituindo todas as ocorrências de **Blrplate** por **MyExpert**.
8.  Edite Resrc1.h renomeando **BLRPLATE** para **MYEXPERT.** (Lembre-se de **que MYEXPERT** deve estar em maiúsculas).
9.  Edite o arquivo MyExpert.rc renomeando **IDD \_ BLRPLATE \_ CONFIG \_ DIALOG** para **IDD \_ MYEXPERT \_ CONFIG \_ DIALOG**.
10. Digite **nmake** para criar o arquivo DLL. Para verificar o build, altere o diretório para o \\ subdiretório Obj e verifique se o arquivo existe. Para obter mais informações, consulte [Exibindo propriedades de DLL especializadas.](viewing-expert-dll-properties.md)

Quando o build for concluído, você terá uma DLL especializada que poderá testar e implantar com Monitor de Rede. Para obter mais informações sobre como instalar um especialista, consulte [Installing an Expert to Monitor de Rede 2.1](installing-an-expert-to-network-monitor-2-1.md). Para obter mais informações sobre como depurar um especialista, consulte [Depurando um especialista.](debugging-an-expert.md)

 

 



