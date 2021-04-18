---
title: Registro automático para controles
description: Registro automático para controles
ms.assetid: 0fff07e5-10bb-4052-8eb1-021efcb66d6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdf2d71dcee1727031dd6ad9d55d88baf86a6b3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105783685"
---
# <a name="self-registration-for-controls"></a>Registro automático para controles

Os controles ActiveX devem dar suporte ao auto-registro implementando as funções [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) . Os controles ActiveX devem registrar todas as entradas de registro padrão para objetos incorporáveis e servidores de automação.

Os controles ActiveX devem usar a API de categorias de componentes para se registrarem como um controle e registrar as categorias de componentes que exigem que um host dê suporte e quaisquer categorias implementadas pelo controle, consulte [categorias de componentes](component-categories.md).

Os controles ActiveX também devem registrar a chave do registro [ToolBoxBitmap32](toolboxbitmap32.md) , embora isso não seja obrigatório.

A categoria de componente que pode ser inserido só deverá ser registrada se o controle for adequado para uso como um objeto de documento composto. É importante observar que um objeto de documento composto deve dar suporte a determinadas interfaces além do [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) mínimo necessário para um controle ActiveX. Embora um controle ActiveX possa ser qualificado como um objeto de documento composto, a documentação do controle deve indicar claramente o comportamento a ser esperado nessas circunstâncias.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controles](controls.md)
</dt> </dl>

 

 