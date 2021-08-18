---
description: Fornece acesso ao contexto de um objeto de cadeia capicor. Esse contexto permite que a cadeia de confiança do certificado capicor seja usada em outras derivações de CryptoAPI.
ms.assetid: ee258586-028e-486e-8129-07f43b6cc468
title: Interface IChainContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5a3ac2f2234c986c9a86073e25e1277fa1af4f10f2809e013bc65849120b90c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005434"
---
# <a name="ichaincontext-interface"></a>Interface IChainContext

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]

A interface **IChainContext** fornece acesso ao contexto de um objeto de [**cadeia**](chain.md) capicor. Esse contexto permite que a cadeia de confiança do certificado capicor seja usada em outras derivações de CryptoAPI.

## <a name="when-to-use"></a>Quando usar

Use essa interface quando precisar usar um objeto de [**cadeia**](chain.md) capicor em outra derivação de CryptoAPI.

## <a name="members"></a>Membros

A interface **IChainContext** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IChainContext** tem esses métodos.



| Método                                           | Descrição                                                                                                                    |
|:-------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**FreeContext**](ichaincontext-freecontext.md) | Libera um contexto de cadeia de PCCERT \_ \_ adquirido por meio da propriedade [**chainContext**](ichaincontext-chaincontext.md) .<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IChainContext** tem essas propriedades.



| Propriedade                                                      | Tipo de acesso           | Descrição                                                               |
|:--------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------|
| [**ChainContext**](ichaincontext-chaincontext.md)<br/> | Leitura/gravação<br/> | Define ou recupera o \_ \_ contexto de cadeia de PCCERT de um certificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




