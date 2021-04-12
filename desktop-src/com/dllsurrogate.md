---
title: DllSurrogate
description: Permite que os servidores DLL sejam executados em um processo substituto. Se uma cadeia de caracteres vazia for especificada, o substituto fornecido pelo sistema será usado; caso contrário, o valor especifica o caminho do substituto a ser usado.
ms.assetid: ae02d828-9cdb-4faa-8fa9-971da97e27b1
keywords:
- COM valor do registro DllSurrogate COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9854f3c4e4390d64d97c8ab829ac2e7fe34488e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366759"
---
# <a name="dllsurrogate"></a>DllSurrogate

Permite que os servidores DLL sejam executados em um processo substituto. Se uma cadeia de caracteres vazia for especificada, o substituto fornecido pelo sistema será usado; caso contrário, o valor especifica o caminho do substituto a ser usado.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogate = path
```

## <a name="remarks"></a>Comentários

Esse é um valor do **reg \_ sz** que especifica que a classe é uma dll a ser ativada em um processo substituto e o processo substituto a ser usado. Para usar o processo de substituição genérico fornecido pelo sistema, defina o *caminho* para uma cadeia de caracteres vazia ou **NULL**. Para especificar outro processo substituto, defina *caminho* para o caminho do substituto. Como na especificação do caminho de um servidor sob a chave [**LocalServer32**](localserver32.md) , uma especificação de caminho completo não é necessária. O substituto deve ser gravado para se comunicar corretamente com o serviço DCOM, conforme descrito em [escrevendo um substituto personalizado](writing-a-custom-surrogate.md).

O valor de **DllSurrogate** deve estar presente para que um servidor dll seja ativado em um substituto. A ativação refere-se a uma chamada para [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex), **CoCreateInstanceEx**, [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile), [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)ou [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject). A execução de DLLs em um processo substituto fornece os benefícios de uma implementação executável, incluindo o isolamento de falhas, a capacidade de atender a vários clientes simultaneamente e permitir que o servidor forneça serviços a clientes remotos em um ambiente distribuído.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[Substitutos de DLL](dll-surrogates.md)
</dt> <dt>

[**DllSurrogateExecutable**](dllsurrogateexecutable.md)
</dt> <dt>

[**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 