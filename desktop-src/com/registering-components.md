---
title: Registrando componentes
description: Registrando componentes
ms.assetid: d7fd231b-17ec-42ad-9144-df7ed5ffb17b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d683ae419466d62d764283cfa8706981de402a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008405"
---
# <a name="registering-components"></a>Registrando componentes

Quando os seguintes tipos de aplicativos são instalados, as informações de instalação devem ser adicionadas ao registro, geralmente por meio de um programa de instalação:

-   Aplicativos de servidor
-   Aplicativos de contêiner/servidor
-   Aplicativos de contêiner que permitem vincular a objetos inseridos

Para todas as três instâncias, registre informações de biblioteca COM (DLL) e informações específicas do aplicativo.

A DLL registra as informações de todos os seus componentes exportando [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver). Use as seguintes funções para registrar e cancelar o registro de um componente:

-   [**Falha em RegOpenKeyEx**](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)
-   [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [**RegSetValueEx**](/windows/desktop/api/winreg/nf-winreg-regsetvalueexa)
-   [**RegEnumKeyEx**](/windows/desktop/api/winreg/nf-winreg-regenumkeyexa)
-   [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya)
-   [**Falha RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando aplicativos COM](registering-com-applications.md)
</dt> </dl>

 

 