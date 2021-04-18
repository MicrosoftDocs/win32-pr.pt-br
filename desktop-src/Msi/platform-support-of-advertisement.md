---
description: O Windows Installer dá suporte ao anúncio de aplicativos e recursos.
ms.assetid: 9e5158bc-4877-49d1-9bb9-4dd17abb444d
title: Suporte de plataforma do anúncio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48016241998473a5bb5ae8ecff05a14fd702f8be
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105751846"
---
# <a name="platform-support-of-advertisement"></a>Suporte de plataforma do anúncio

O Windows Installer dá suporte ao anúncio de aplicativos e recursos.

Os seguintes recursos de anúncio estão disponíveis no Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP e Windows 2000.

-   Atalhos e seus ícones.

-   Extensões e seus ícones especificados na [tabela ProgID](progid-table.md).

-   Verbos de shell e comando registrados sob a chave ProgId.

-   Contextos de CLSID e InProcHandler.

-   A instalação sob demanda por meio de OLE só está disponível programaticamente por meio de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (C/C++) e da **função CreateObject (Visual Basic)** ou da **função GetObject (Visual Basic)**.

> [!Note]
> As informações de AppId e TypeLib são gravadas somente quando um componente anunciado é instalado.
> 
> Para dar suporte a extensões de nome de arquivo, o aplicativo deve ser publicado para Active Directory por um administrador usando Política de Grupo.

## <a name="remarks"></a>Comentários

A instalação do produto pode não exigir uma reinicialização, mas os atalhos anunciados não funcionam até que o computador seja reiniciado. Os atalhos anunciados das instalações subsequentes funcionam sem uma reinicialização.

Para garantir que os atalhos anunciados funcionem corretamente, o autor do pacote deve agendar uma reinicialização forçada no final da instalação.

Para evitar reinicializações desnecessárias do sistema, agende uma reinicialização para ser executada somente se nenhuma versão do Windows Installer estiver instalada.

As instruções condicionais podem verificar a propriedade [**ShellAdvtSupport**](shelladvtsupport.md) e a propriedade [**Version9X**](version9x.md) . Para obter mais informações sobre como agendar reinicializações forçadas condicionais, consulte [reinicializações do sistema](system-reboots.md) e [uso de propriedades em instruções condicionais](using-properties-in-conditional-statements.md).

 

 
