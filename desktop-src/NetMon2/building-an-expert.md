---
description: Este tópico descreve como criar um especialista genérico que é fornecido com o SDK do Monitor de Rede.
ms.assetid: c05b261d-3fac-40bf-b4ff-bd766f8d148f
title: Criando um especialista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ead0ff222b72c66bfc88ec477d1a8d6a941273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169380"
---
# <a name="building-an-expert"></a>Criando um especialista

Este tópico descreve como criar um especialista genérico que é fornecido com o SDK do Monitor de Rede.

> [!Note]  
> Antes de criar os exemplos de código a seguir, instale o SDK do Monitor de Rede e inicialize o arquivo de MySetEnv.bat.

 

**Para criar um especialista genérico**

1.  Abra um prompt de comando Monitor de Rede e navegue até o \\ subdiretório experts; por exemplo, C: \\ Program Files \\ NetMonSDK2 \\ experts.
2.  Digite **Xcopy/e/s/V Blrplate MyExpert**; em seguida, quando solicitado, digite **D**.
3.  Mova para o \\ subdiretório MyExpert.
4.  Digite **Ren Blrplate \* . \* MyExpert \* . \***. Verifique se todos os arquivos foram renomeados corretamente. Verifique os nomes de arquivo comparando os arquivos \\ no \\ subdiretório experts Blrplate.
5.  Edite o makefile substituindo todas as ocorrências de **Blrplate** por **MyExpert**.
6.  Edite ambos os arquivos. cpp substituindo todas as ocorrências de **Blrplate** por **MyExpert**. Lembre-se de que o identificador da caixa de diálogo em config. cpp deve estar em letras maiúsculas (por exemplo, **MyExpert**).
7.  Edite MyExpert. h substituindo todas as ocorrências de **Blrplate** por **MyExpert**.
8.  Edite Resrc1. h renomeando **BLRPLATE** para **MyExpert**. (Lembre-se de que **MyExpert** deve estar em letras maiúsculas).
9.  Edite o arquivo MyExpert. rc ao renomear a **\_ caixa de diálogo IDD BLRPLATE \_ config \_** para a **caixa de \_ \_ \_ diálogo configuração do IDD MyExpert**.
10. Digite **NMAKE** para criar o arquivo dll. Para verificar a compilação, altere o diretório para o \\ subdiretório obj e verifique se o arquivo existe. Para obter mais informações, consulte [exibindo Propriedades de DLL de especialistas](viewing-expert-dll-properties.md).

Quando a compilação for concluída, você terá uma DLL de especialista que pode ser testada e implantada com Monitor de Rede. Para obter mais informações sobre como instalar um especialista, consulte [instalando um especialista para Monitor de Rede 2,1](installing-an-expert-to-network-monitor-2-1.md). Para obter mais informações sobre como depurar um especialista, consulte [Depurando um especialista](debugging-an-expert.md).

 

 



