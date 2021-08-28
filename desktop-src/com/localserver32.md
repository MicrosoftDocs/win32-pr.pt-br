---
title: LocalServer32
description: Especifica o caminho completo para um aplicativo de servidor local de 32 bits.
ms.assetid: 5d922230-f53d-4bf9-be50-c8c00f45b7a8
keywords:
- COM chave do registro LocalServer32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105cb352ffa3833c59e5ee8d042689e82e77b29dbcea7e49608d0047876bdd37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859396"
---
# <a name="localserver32"></a>LocalServer32

Especifica o caminho completo para um aplicativo de servidor local de 32 bits.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer32
         (Default) = path
         ServerExecutable = path
```

## <a name="remarks"></a>Comentários

o valor **ServerExecutable** , que é do tipo **REG \_ SZ** e tem suporte a partir do Windows Server 2003, funciona em conjunto com a subchave **LocalServer32** para evitar qualquer ambiguidade ao usar a função [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) . **LocalServer32** especifica o local do aplicativo de servidor com a ser iniciado, e essas informações são passadas como o primeiro parâmetro *lpApplicationName* para **CreateProcess**. Dependendo da implementação de **CreateProcess**, essas informações podem ser ambíguas. Por esse motivo, se **ServerExecutable** for especificado, com passará o valor nomeado **ServerExecutable** para o parâmetro *lpApplicationName* de **CreateProcess**. Se **ServerExecutable** não for especificado, com passará **NULL** como o valor para o primeiro parâmetro de **CreateProcess**.

Para ajudar a fornecer segurança do sistema, use cadeias de caracteres entre aspas no caminho para indicar onde o nome do arquivo executável termina e os argumentos começam. Por exemplo, em vez de especificar o seguinte caminho como a entrada **LocalServer32** :

"C: \\ arquivos de programa \\ arquivos da empresa \\Application.exe param1 param2"

Especifique o caminho usando a seguinte sintaxe:

" \\ C: \\ Program Files \\ arquivos da empresa \\Application.exe\\ " param1 param2 "

COM anexa o sinalizador "-incorporando" à cadeia de caracteres, de modo que o aplicativo que usa sinalizadores precisa analisar toda a cadeia de caracteres e verificar o sinalizador de incorporação.

Quando o COM inicia um servidor local de 32 bits, o servidor deve registrar um objeto de classe dentro de um tempo decorrido definido pelo usuário. Por padrão, o valor de tempo decorrido deve ser de pelo menos 5 minutos, em milissegundos, mas não pode exceder o número de milissegundos em 30 dias. Normalmente, os aplicativos não devem definir esse valor, que está na entrada **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ COM2 \\ ServerStartElapsedTime** .

As entradas necessárias para servidores locais de 32 bits são [**InprocHandler32**](inprochandler32.md), [**LocalServer**](localserver.md), **LocalServer32** e [**insertáveis**](insertable.md).

Se um contêiner estiver pesquisando o registro de um servidor local, um servidor local de 32 bits terá prioridade sobre um servidor local de 16 bits.

Se você estiver implementando classes como serviços, deve estar ciente de que o [**LocalService**](localservice.md) nomeado Value é usado em preferência à chave **LocalServer32** para ativação local e remota requestsâ € "se o **LocalService** existir e se referir a um serviço válido, a chave **LocalServer32** será ignorada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**LocalServer**](localserver.md)
</dt> <dt>

[**LocalService**](localservice.md)
</dt> </dl>

 

 