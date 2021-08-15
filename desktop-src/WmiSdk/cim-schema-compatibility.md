---
description: Compatibilidade do esquema CIM
ms.assetid: 3738914d-dd33-4999-b37f-b4bb94689cd4
ms.tgt_platform: multiple
title: Compatibilidade do esquema CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3d87f1e40a52998f3a53a9b06f0572d8916b4a53663354ca5ffde67beaeed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319782"
---
# <a name="cim-schema-compatibility"></a>Compatibilidade do esquema CIM

um componente fundamental da infraestrutura de Instrumentação de Gerenciamento do Windows (WMI) é um modelo orientado a objeto das entidades gerenciáveis em um sistema. O modelo está em conformidade com um padrão mantido pelo Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) e é conhecido como o modelo CIM (CIM). O esquema CIM fornece um mecanismo de descrição de dados único para todos os dados que eles fornecem.

a partir do Windows 7, o WMI é compatível com a versão do esquema CIM 2.17.1 ( [https://www.dmtf.org/standards/cim/cim\_schema\_v2171/](https://www.dmtf.org/standards/cim/cim_schema_v2171) ). agora, os usuários podem compilar um esquema definido por DMTF em um computador Windows.

## <a name="benefits-of-cim-schema-version-2171-compatibility"></a>Benefícios da compatibilidade de 2.17.1 da versão do esquema CIM

-   quando um usuário baixa a versão do esquema CIM 2.17.1 ou arquivos MOF do DMTF, eles podem ser compilados com êxito no computador de destino Windows.
-   A versão do esquema CIM 2.17.1 adicionou suporte para BIOS, impressoras, mensagens padrão, estado do sistema operacional, paradigmas de gerenciamento de energia modernos, virtualização e segurança.
-   A versão do esquema CIM 2.1.7.1 oferece suporte a perfil adicional. Para obter mais informações, consulte [passagem de associação de namespace cruzado](cross-namespace-association-traversal.md)

 

 



