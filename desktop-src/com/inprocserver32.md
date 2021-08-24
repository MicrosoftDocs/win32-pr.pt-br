---
title: Inprocserver32
description: Registra um servidor em processo de 32 bits e especifica o modelo de threading do apartment no qual o servidor pode executar.
ms.assetid: 4edbbd9d-7ea1-4476-aee7-eaf30e54db8d
keywords:
- Chave do Registro InprocServer32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9904aa636bbfb8dc0bc01cac85e041aedfcd34364bd62ac7b0e4e5a9f904750f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567816"
---
# <a name="inprocserver32"></a>Inprocserver32

Registra um servidor em processo de 32 bits e especifica o modelo de threading do apartment no qual o servidor pode executar.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         (Default) = path
         ThreadingModel = value
```

## <a name="remarks"></a>Comentários

**ThreadingModel é** um **valor REG \_ SZ** que especifica o modelo de threading. Os valores possíveis são mostrados na tabela a seguir.



| Valor     | Descrição                                |
|-----------|--------------------------------------------|
| Apartamento | Apartment de thread único                  |
| Ambos      | Apartment de thread único ou multithread |
| Gratuito      | Apartment multithreaded                    |
| Neutro   | Apartment neutro                          |



 

Você deve usar o mesmo valor para cada objeto fornecido pelo servidor em processo.

Se **ThreadingModel** não estiver presente ou não estiver definido como um valor, o servidor será carregado no primeiro apartment que foi inicializado no processo. Às vezes, esse apartment é conhecido como STA (single-threaded apartment) principal. Se o primeiro STA em um processo for inicializado por COM, em vez de por uma chamada explícita para [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), ele será chamado de STA do host. Por exemplo, COM cria um STA de host se um servidor em processo a ser carregado requer um STA, mas atualmente não há STA no processo.

Sempre que possível, o servidor em processo é carregado no mesmo apartment que o cliente que o carrega. Se o modelo de threading do apartment do cliente não for compatível com o modelo especificado, o servidor será carregado conforme indicado na tabela a seguir.



| Modelo de threading do servidor | O servidor apartment é executado no |
|---------------------------|----------------------------|
| <not specified>     | STA principal                   |
| Ambos                      | Mesmo apartment que o cliente   |
| Gratuito                      | Apartment multithreaded    |
| Neutro                   | Apartment neutro          |



 

Se o modelo de threading do servidor for Apartment, o apartment no qual o servidor será carregado dependerá do apartment no qual o cliente está executando, conforme indicado na tabela a seguir.



| O cliente apartment é executado no | O servidor apartment é executado no |
|----------------------------|----------------------------|
| Multithread              | Host STA                   |
| Neutro (no thread STA)    | Mesmo apartment que o cliente   |
| Neutro (no thread MTA)    | Host STA                   |



 

O COM também pode criar um host MTA (multithreaded apartment). Se um cliente em um apartment de thread único solicitar um servidor em processo cujo modelo de threading é Gratuito quando não há MTA no processo, o COM cria um host MTA e carrega o servidor nele.

Para um servidor em processo de 32 bits, as chaves [**InprocHandler32,**](inprochandler32.md) [**InprocServer,**](inprocserver.md) **InprocServer32** e [**Insertable**](insertable.md) devem ser registradas. A **entrada InprocServer** é necessária apenas para compatibilidade com backward. Se estiver ausente, a classe ainda funcionará, mas não poderá ser carregada em aplicativos de 16 bits.

Se um contêiner estiver pesquisando no Registro um servidor em processo, a versão de 16 bits terá prioridade com um contêiner de 16 bits e a versão de 32 bits terá prioridade com um contêiner de 32 bits.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**InprocServer**](inprocserver.md)
</dt> </dl>

 

 




