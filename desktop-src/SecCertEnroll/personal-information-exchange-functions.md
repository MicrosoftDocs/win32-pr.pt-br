---
description: cada uma das seções a seguir discute uma função exportada por Xenroll.dll para gerenciar mensagens de Exchange PFX (informações pessoais).
ms.assetid: f7e6b3a6-eae4-49f8-a624-609742741560
title: funções de Exchange de informações pessoais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1e7cddcda00131b64c5fe6122d777695bbab4f80cbac8e71648a2197fed036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774679"
---
# <a name="personal-information-exchange-functions"></a>funções de Exchange de informações pessoais

cada uma das seções a seguir discute uma função exportada por Xenroll.dll para gerenciar mensagens de Exchange PFX (informações pessoais). Cada seção também aborda como usar CertEnroll.dll para substituir a função ou indica que não existe nenhum mapeamento entre as duas bibliotecas.

## <a name="createfilepfxwstr"></a>createFilePFXWStr

A função [**createFilePFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) no Xenroll.dll salva uma cadeia de certificados e uma [*chave privada*](/windows/desktop/SecGloss/p-gly) em um arquivo usando o formato PFX.

A biblioteca de CertEnroll.dll não implementa diretamente a funcionalidade para copiar a mensagem PFX em um arquivo. No entanto, você pode usar o método [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) na interface [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para criar uma mensagem pfx codificada e gravar uma função personalizada para salvar a mensagem em um arquivo.

## <a name="createpfxwstr"></a>createPFXWStr

A função [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) no Xenroll.dll salva uma cadeia de certificados e uma chave privada em uma cadeia de caracteres de formato PFX.

Você pode usar o método [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) na interface [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para criar uma mensagem pfx codificada que contém a cadeia de certificados e a chave. Você pode especificar uma senha, opções de exportação e tipo de codificação. Para recuperar uma cadeia de caracteres equivalente à retornada de [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr), passe o \_ \_ sinalizador binário de cadeia de caracteres cript XCN \_ no parâmetro de *codificação* do método [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeando Xenroll.dll para CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
