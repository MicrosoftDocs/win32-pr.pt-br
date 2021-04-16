---
title: InprocServer32
description: Registra um servidor em processo de 32 bits e especifica o modelo de Threading do apartamento no qual o servidor pode ser executado.
ms.assetid: 4edbbd9d-7ea1-4476-aee7-eaf30e54db8d
keywords:
- A chave do registro InprocServer32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daae9d495ad588e0dc710b63fe7d7ae9f48c11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498768"
---
# <a name="inprocserver32"></a>InprocServer32

Registra um servidor em processo de 32 bits e especifica o modelo de Threading do apartamento no qual o servidor pode ser executado.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         (Default) = path
         ThreadingModel = value
```

## <a name="remarks"></a>Comentários

**ThreadingModel** é um valor de **\_ sz de reg** que especifica o modelo de Threading. Os valores possíveis são mostrados na tabela a seguir.



| Valor     | Descrição                                |
|-----------|--------------------------------------------|
| Sta | Apartamento de thread único                  |
| Ambos      | Apartamento de thread único ou multithread |
| Gratuita      | Apartamento multithread                    |
| Neutro   | Apartamento neutro                          |



 

Você deve usar o mesmo valor para cada objeto fornecido pelo servidor em processo.

Se **ThreadingModel** não estiver presente ou não estiver definido como um valor, o servidor será carregado no primeiro apartamento que foi inicializado no processo. Esse apartamento às vezes é chamado de STA (single-threaded apartment). Se o primeiro STA em um processo for inicializado por COM, em vez de uma chamada explícita para o [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), ele será chamado de Sta do host. Por exemplo, COM cria um host STA se um servidor em processo a ser carregado requer um STA, mas atualmente não há um STA no processo.

Sempre que possível, o servidor em processo é carregado no mesmo apartamento que o cliente que o carrega. Se o modelo de Threading do apartamento do cliente não for compatível com o modelo especificado, o servidor será carregado conforme indicado na tabela a seguir.



| Modelo de Threading do servidor | O servidor de apartamento é executado em |
|---------------------------|----------------------------|
| <not specified>     | STA principal                   |
| Ambos                      | Mesmo apartamento como cliente   |
| Gratuita                      | Apartamento multithread    |
| Neutro                   | Apartamento neutro          |



 

Se o modelo de Threading do servidor for Apartment, o apartamento no qual o servidor é carregado dependerá do apartamento em que o cliente está sendo executado, conforme indicado na tabela a seguir.



| O cliente de apartamento é executado em | O servidor de apartamento é executado em |
|----------------------------|----------------------------|
| Multithread              | Host STA                   |
| Neutro (no thread STA)    | Mesmo apartamento como cliente   |
| Neutro (no thread MTA)    | Host STA                   |



 

COM também pode criar um MTA (multithreaded apartment) do host. Se um cliente em um apartamento de thread único solicitar um servidor em processo cujo modelo de Threading seja gratuito quando não houver MTA no processo, o COM criará um MTA de host e carregará o servidor nele.

Para um servidor em processo de 32 bits, as chaves [**InprocHandler32**](inprochandler32.md), [**InprocServer**](inprocserver.md), **InprocServer32** e [**Insertable**](insertable.md) devem ser registradas. A entrada **InprocServer** é necessária apenas para compatibilidade com versões anteriores. Se ele estiver ausente, a classe ainda funcionará, mas não poderá ser carregada em aplicativos de 16 bits.

Se um contêiner estiver pesquisando o registro de um servidor em processo, a versão de 16 bits terá prioridade com um contêiner de 16 bits e a versão de 32 bits terá prioridade com um contêiner de 32 bits.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**InprocServer**](inprocserver.md)
</dt> </dl>

 

 




