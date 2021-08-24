---
description: Fornece métodos COM padrão para gerenciar itens de dados de armazenamento protegidos.
ms.assetid: 6a4200ed-c3cf-4d6c-8936-22261e670087
title: Interface IPStore (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d6404d182a0c46de222b64892caa8b0e853610c980bfb79d286f781277493cba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749702"
---
# <a name="ipstore-interface"></a>Interface IPStore

\[o Armazenamento protegido (pstore) está disponível para uso no Windows Server 2003 e no Windows XP. ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

\[Essa interface pode ser alterada ou indisponível em versões futuras do Windows.\]

Fornece métodos COM padrão para gerenciar itens de dados de armazenamento protegidos. O método [**PStoreCreateInstance**](pstorecreateinstance.md) retorna um ponteiro para essa interface.

## <a name="members"></a>Membros

A interface **IPStore** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IPStore** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IPStore** tem esses métodos.



| Método                                                   | Descrição                                                                                                           |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**CloseItem**](ipstore-closeitem.md)                   | Fecha um item de dados especificado do armazenamento protegido.<br/>                                                       |
| [**CreateSubtype**](ipstore-createsubtype.md)           | Cria o subtipo especificado dentro do tipo especificado.<br/>                                                   |
| [**CreateType**](ipstore-createtype.md)                 | Cria o tipo especificado com o nome especificado.<br/>                                                        |
| [**DeleteItem**](ipstore-deleteitem.md)                 | Exclui o item especificado do armazenamento protegido.<br/>                                                     |
| [**DeleteSubtype**](ipstore-deletesubtype.md)           | Exclui o subtipo de item especificado do armazenamento protegido.<br/>                                             |
| [**Excluirtype**](ipstore-deletetype.md)                 | Exclui o tipo especificado do armazenamento protegido.<br/>                                                     |
| [**EnumItems**](ipstore-enumitems.md)                   | Retorna o ponteiro de interface de um subtipo para enumerar itens no banco de dados de armazenamento protegido.<br/>        |
| [**EnumSubtypes**](ipstore-enumsubtypes.md)             | Retorna uma interface para enumerar subtipos dos tipos atualmente registrados no banco de dados protegido.<br/> |
| [**EnumTypes**](ipstore-enumtypes.md)                   | Retorna uma interface para enumerar os tipos atualmente registrados no banco de dados protegido.<br/>             |
| [**GetInfo**](ipstore-getinfo.md)                       | Recupera informações sobre o provedor de armazenamento.<br/>                                                          |
| [**GetProvParam**](ipstore-getprovparam.md)             | Não implementado.<br/>                                                                                           |
| [**GetSubtypeInfo**](ipstore-getsubtypeinfo.md)         | Recupera informações associadas a um subtipo.<br/>                                                           |
| [**GetTypeInfo**](ipstore-gettypeinfo.md)               | Recupera informações associadas a um tipo.<br/>                                                              |
| [**OpenItem**](ipstore-openitem.md)                     | Abre um item para vários acessos.<br/>                                                                       |
| [**ReadAccessRuleSet**](ipstore-readaccessruleset.md)   | Não implementado.<br/>                                                                                           |
| [**ReadItem**](ipstore-readitem.md)                     | Lê o item de dados especificado do armazenamento protegido.<br/>                                                      |
| [**SetProvParam**](ipstore-setprovparam.md)             | Define as informações do parâmetro especificado.<br/>                                                                  |
| [**WriteAccessRuleset**](ipstore-writeaccessruleset.md) | Não implementado.<br/>                                                                                           |
| [**WriteItem**](ipstore-writeitem.md)                   | Grava um item de dados no armazenamento protegido.<br/>                                                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
