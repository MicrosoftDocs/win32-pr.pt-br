---
description: 'Os valores do registro WFP estão localizados na seguinte chave do registro: HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon.'
ms.assetid: d4da7f24-1e5d-4ea2-98e8-049e7eaefae1
title: Valores de registro de WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb8db23800ebbead68f34eaf0fa9fffd772f01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758263"
---
# <a name="wfp-registry-values"></a>Valores de registro de WFP

\[Não há suporte para valores de registro WFP a partir do Windows Vista.\]

A WFP usa vários valores de registro para configurações de personalização. Os valores do registro WFP estão localizados na seguinte chave do registro:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
```

A seguir estão os valores do registro WFP.

<dl> <dt>

<span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**
</dt> <dd>

Local do cache. Esse deve ser um caminho local. O valor padrão é% SystemRoot% \\ System32 \\ dllcache.

</dd> <dt>

<span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**
</dt> <dd>

Opções de cota. Esse valor de registro pode ser um dos valores a seguir.



| Valor                  | Significado                                                  |
|------------------------|----------------------------------------------------------|
| \_ \_ todos os arquivos da cota Sfc \_ | O tamanho do cache de DLL é ilimitado. Esse é o padrão. |
| Outros valores           | Tamanho do cache de DLL, em arquivos.                         |



 

</dd> <dt>

<span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SFCScan**
</dt> <dd>

Opções de verificação. Esse valor de registro pode ser um dos valores a seguir.



| Valor             | Significado                                                   |
|-------------------|-----------------------------------------------------------|
| \_verificação \_ normal do Sfc | Não verificar arquivos protegidos na inicialização. Esse é o padrão. |
| verificação de SFC \_ \_ sempre | Verificar arquivos protegidos em cada inicialização.                       |
| verificação de SFC \_ \_ uma vez   | Verificar arquivos protegidos na próxima inicialização.                    |



 

</dd> </dl>

 

 



