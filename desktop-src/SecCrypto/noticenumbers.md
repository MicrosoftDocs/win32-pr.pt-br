---
description: Representa uma coleção de objetos de extensão.
ms.assetid: b0d69df9-12c4-4872-b883-b029c4350502
title: Objeto NoticeNumbers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 58d954fdeef66d6d0e5eadb3086cb549b59e5669
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779356"
---
# <a name="noticenumbers-object"></a>Objeto NoticeNumbers

\[O objeto **NoticeNumbers** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Para obter mais informações, consulte [**qualificador**](qualifier.md).\]

O objeto **NoticeNumbers** representa uma coleção de objetos de [**extensão**](extension.md) . Cada objeto de [**extensão**](extension.md) representa um número de aviso do usuário.

## <a name="when-to-use"></a>Quando usar

O objeto **NoticeNumbers** é usado para executar as seguintes tarefas:

-   Recupere o número de objetos de [**extensão**](extension.md) na coleção.
-   Recupere um objeto de [**extensão**](extension.md) específico da coleção.
-   Iterar pela coleção.

## <a name="members"></a>Membros

O objeto **NoticeNumbers** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **NoticeNumbers** tem essas propriedades.



| Propriedade                                              | Tipo de acesso          | Descrição                                                                                                                                                                                                                     |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](noticenumbers-newenum.md)<br/> | Somente leitura<br/> | Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção. Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contar**](noticenumbers-count.md)<br/>       | Somente leitura<br/> | Recupera o número de objetos de [**extensão**](extension.md) na coleção.<br/>                                                                                                                                    |
| [**Item**](noticenumbers-item.md)<br/>         | Somente leitura<br/> | Recupera o objeto de [**extensão**](extension.md) que representa o número de aviso indexado da coleção.<br/> Essa é a propriedade padrão.<br/>                                                            |



 

## <a name="remarks"></a>Comentários

O objeto **NoticeNumbers** não pode ser criado.

O objeto NoticeNumbers é usado na propriedade [**Qualifier. NoticeNumbers**](qualifier-noticenumbers.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
