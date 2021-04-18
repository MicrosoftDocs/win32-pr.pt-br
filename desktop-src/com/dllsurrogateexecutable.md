---
title: DllSurrogateExecutable
description: Permite que os servidores DLL sejam executados em um processo substituto personalizado, em conjunto com o valor do registro DllSurrogate. Se DllSurrogateExecutable não for especificado, COM passará NULL como o valor do primeiro parâmetro da função CreateProcess.
ms.assetid: faf5dde3-bd67-447b-a88c-e8660dc5228e
keywords:
- COM valor do registro DllSurrogateExecutable COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877297673b0a518006ecf903f447984f9023da34
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105764154"
---
# <a name="dllsurrogateexecutable"></a>DllSurrogateExecutable

Permite que os servidores DLL sejam executados em um processo substituto personalizado, em conjunto com o valor do registro [**DllSurrogate**](dllsurrogate.md) . Se **DllSurrogateExecutable** não for especificado, com passará **NULL** como o valor do primeiro parâmetro da função [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogateExecutable = file
```

## <a name="remarks"></a>Comentários

Esse valor é do tipo **reg \_ sz**. Ele funciona em conjunto com o valor [**DllSurrogate**](dllsurrogate.md) para evitar qualquer ambiguidade ao usar a função [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) . **DllSurrogate** indica se um substituto personalizado precisa ser usado e essas informações são passadas como o primeiro parâmetro para **CreateProcess**. Dependendo da implementação de **CreateProcess**, essas informações podem ser ambíguas. Se **DllSurrogateExecutable** for especificado, com passará o valor como o primeiro parâmetro de **CreateProcess**. Se **DllSurrogateExecutable** não for especificado, com passará **NULL** como o valor para o primeiro parâmetro de **CreateProcess**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[Substitutos de DLL](dll-surrogates.md)
</dt> <dt>

[**DllSurrogate**](dllsurrogate.md)
</dt> <dt>

[**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 