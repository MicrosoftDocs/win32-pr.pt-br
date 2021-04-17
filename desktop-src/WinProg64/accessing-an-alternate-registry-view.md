---
title: Acessando uma exibição alternativa do registro
description: Por padrão, um aplicativo de 32 bits em execução no WOW64 acessa a exibição do registro de 32 bits e um aplicativo de 64 bits acessa a exibição do registro de 64 bits.
ms.assetid: 2c5fd3de-998c-44ab-863e-8e0e90d56e5d
keywords:
- o registro exibe a programação de 64 bits do Windows
- Programação WOW64 de 64 bits do Windows, exibições do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3bca57367394e1b2fffc6486065e93c966f224
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "105797650"
---
# <a name="accessing-an-alternate-registry-view"></a>Acessando uma exibição alternativa do registro

Por padrão, um aplicativo de 32 bits em execução no WOW64 acessa a exibição do registro de 32 bits e um aplicativo de 64 bits acessa a exibição do registro de 64 bits. Os sinalizadores a seguir permitem que aplicativos de 32 bits acessem chaves redirecionadas na exibição do registro de 64 bits e aplicativos de 64 bits para acessar chaves redirecionadas na exibição de registro de 32 bits. Esses sinalizadores não têm nenhum efeito em chaves de registro compartilhadas. Para obter mais informações, consulte [chaves do registro afetadas pelo WOW64](shared-registry-keys.md).



| Nome do sinalizador         | Valor  | Descrição                                                                                                                                                                                                                                       |
|-------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CHAVE \_ 64KEY de WOW64 \_ | 0x0100 | Acesse uma chave de 64 bits de um aplicativo de 32 bits ou de 64 bits.                                                                                                                                                                                   |
| CHAVE \_ 32KEY de WOW64 \_ | 0x0200 | Acesse uma chave de 32 bits de um aplicativo de 32 bits ou de 64 bits.<br/>**Windows 10 no ARM:** Isso se refere à exibição do registro ARM de 32 bits para processos ARM de 32 bits e a exibição do registro do x86 de 32 bits para processos de ARM64 de 32 bits e de 64 bits. |



 

Esses sinalizadores podem ser especificados no parâmetro *samDesired* das seguintes funções de registro:

-   [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [**RegDeleteKeyEx**](/windows/desktop/api/winreg/nf-winreg-regdeletekeyexa)
-   [**Falha em RegOpenKeyEx**](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)

O \_ \_ 32KEY de WOW64 de chave ou 64KEY de WOW64 de chave \_ \_ podem ser especificados. Se ambos os sinalizadores forem especificados, a função falhará com o parâmetro de erro \_ inválido \_ .

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Se ambos os sinalizadores forem especificados, o comportamento da função s será indefinido.

A função [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) não pode ser usada para acessar uma exibição de registro alternativa.

Veja a seguir as práticas recomendadas ao acessar o registro de um aplicativo:

-   Depois que o aplicativo tiver acessado uma exibição alternativa do registro usando um dos sinalizadores, todas as operações subsequentes (criar, excluir ou abrir) nas chaves do registro filho deverão usar explicitamente o mesmo sinalizador. Caso contrário, pode haver um comportamento inesperado.
-   Para enumerar com precisão todas as chaves em ambos os modos de exibição, execute a enumeração em duas passagens. A primeira passagem deve usar um identificador aberto com um dos sinalizadores e a outra passa usar um identificador aberto com o outro sinalizador.

> [!Note]  
> As chaves **Wow6432Node** e **WowAA32Node** são reservadas. Para compatibilidade, os aplicativos não devem usar essas chaves diretamente.

 

Para obter informações sobre como acessar a exibição alternativa do registro por meio do WMI, consulte [solicitando dados WMI em uma plataforma de 64 bits](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Redirecionador de registro](registry-redirector.md)
</dt> <dt>

[Reflexão do registro](registry-reflection.md)
</dt> </dl>

 

