---
title: DllSurrogateExecutable
description: Permite que os servidores DLL executem em um processo substituto personalizado, em conjunto com o valor do Registro DllSurrogate. Se DllSurrogateExecutable não for especificado, COM passará NULL como o valor para o primeiro parâmetro da função CreateProcess.
ms.assetid: faf5dde3-bd67-447b-a88c-e8660dc5228e
keywords:
- Valor do Registro DllSurrogateExecutable COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fc12af22d1f85c2d2e5ff6e75b2904c5fc5eea636a64e314f997ff36a44e38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119373376"
---
# <a name="dllsurrogateexecutable"></a>DllSurrogateExecutable

Permite que os servidores DLL executem em um processo substituto personalizado, em conjunto com o valor do Registro [**DllSurrogate.**](dllsurrogate.md) Se **DllSurrogateExecutable** não for especificado, COM passará **NULL** como o valor para o primeiro parâmetro da [**função CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogateExecutable = file
```

## <a name="remarks"></a>Comentários

Esse valor é do tipo **REG \_ SZ.** Ele funciona em conjunto com o [**valor DllSurrogate**](dllsurrogate.md) para evitar qualquer ambiguidade ao usar a [**função CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) **DllSurrogate** indica se um substituto personalizado precisa ser usado e essas informações são passadas como o primeiro parâmetro **para CreateProcess**. Dependendo da implementação de **CreateProcess**, essas informações podem ser ambíguas. Se **DllSurrogateExecutable** for especificado, COM passará o valor como o primeiro parâmetro de **CreateProcess.** Se **DllSurrogateExecutable** não for especificado, COM passará **NULL** como o valor para o primeiro parâmetro de **CreateProcess.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[Substitutos de DLL](dll-surrogates.md)
</dt> <dt>

[**DllSurrogate**](dllsurrogate.md)
</dt> <dt>

[**Isurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 