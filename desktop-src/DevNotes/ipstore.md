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
ms.openlocfilehash: 4193e21255445c397bfab6439c4890789b8c5562
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751957"
---
# <a name="ipstore-interface"></a>Interface IPStore

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

\[Essa interface pode ser alterada ou não estar disponível em versões futuras do Windows.\]

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



 

 
