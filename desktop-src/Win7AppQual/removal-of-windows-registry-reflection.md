---
description: Remoção da reflexão do registro do Windows
ms.assetid: 4b42d44d-cde8-4d96-96c5-24b7ab7e4cec
title: Remoção da reflexão do registro do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeab0109cbbac988c89d6add91fa899cea9169ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116254"
---
# <a name="removal-of-windows-registry-reflection"></a>Remoção da reflexão do registro do Windows

## <a name="platform"></a>Plataforma

**Clientes** -Windows 7  
**Servidores** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** -baixa  
**Frequência** -baixa  





## <a name="description"></a>Descrição

O processo de reflexão do registro copia chaves e valores do registro entre duas exibições do registro para mantê-las em sincronia. Nas instalações anteriores de 64 bits do Windows, o processo refletiu um subconjunto das chaves do registro redirecionadas entre as exibições de 32 bits e 64 bits. No entanto, a implementação disso causou algumas inconsistências no estado do registro. (Para obter detalhes sobre a reflexão do registro, consulte o artigo correspondente do MSDN na seção *links para outros recursos* abaixo.)

A partir do Windows 7, removemos completamente a reflexão do registro e mesclamos as chaves que costumava ser refletidas:

-   HKEY \_ local \_ Machine \\ software \\ classes
-   HKEY \_ local \_ Machine \\ software \\ Microsoft \\ com3
-   HKEY \_ local \_ Machine \\ software \\ Microsoft \\ EventSystem
-   HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE
-   HKEY \_ local \_ Machine \\ software \\ Microsoft \\ RPC
-   HKey \_ usuários \\ \* \\ classes de software \\
-   \_Classes de usuários hKey \\ \* \_

Efetivamente, isso fornece o mesmo comportamento de reflexão, pois as alterações a essas chaves imediatamente estão disponíveis para aplicativos de 32 bits e de 64 bits.

As chaves que foram refletidas condicionalmente permanecem divididas:

-   HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID
-   HKEY \_ local \_ Machine \\ software \\ classes \\ interface
-   O hKey \_ Users \\ \* \\ classes de software \\ \\ CLSID
-   HKey \_ Users \\ \* \\ \\ interface classes de software \\
-   \_CLSID de \\ \* \_ classes \\ de usuários hKey
-   \_Interface de \\ \* \_ classes \\ de usuários hKey

Eles são usados para manter os dados que não devem ser compartilhados entre aplicativos de 32 bits e de 64 bits.

## <a name="manifestation"></a>Manifestação

As chaves CLSID e de interface da lista acima não são mais refletidas enquanto ainda são redirecionadas. Embora esse seja o comportamento desejado na maioria dos casos, é possível que os aplicativos possam assumir uma dependência do comportamento refletido no vista.

As funções que permitem que os aplicativos controlem a reflexão (RegDisableReflectionKey e RegEnableReflectionKey) são não Ops no Windows 7.

## <a name="mitigation-of-impact"></a>Mitigação do impacto

COM é o principal consumidor de reflexão de registro. COM e outros consumidores foram atualizados para acomodar essa alteração. Essa alteração não afeta os aplicativos que usam APIs COM padrão.

## <a name="solution"></a>Solução

Aplique uma das opções a seguir se você estiver contando com a reflexão do registro para sincronizar as exibições de 32 bits e 64 bits:

-   Criar chaves em ambas as exibições explicitamente durante a instalação
-   Mover as chaves para fora do escopo das chaves refletidas
-   Verificar as duas exibições do registro ao consultar uma chave refletida

    **Observação:** CHAVE \_ \_ 32KEY de WOW64 e \_ sinalizadores de 64KEY de WOW64 principais \_ não podem ser combinados

Aplique uma das opções a seguir se você estiver contando com as funções RegDisableReflectionKey para desabilitar a reflexão do registro:

-   Criar chaves em ambas as exibições explicitamente durante a instalação
-   Mover as chaves para fora do escopo das chaves refletidas
-   Usar subchaves específicas da plataforma (como x86, AMD64 e IA64) para separar dados específicos de um bit de bits

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Artigo de reflexo do registro](../winprog64/registry-reflection.md)
-   [Lista de chaves redirecionadas no artigo redirecionador do registro](../winprog64/registry-redirector.md)
-   [Práticas recomendadas para o WOW64](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)

> [!Note]  
> Esses recursos podem não estar disponíveis em alguns idiomas e países/regiões.

 

 

 
