---
description: Representa um produto. Isso inclui software e hardware usado neste sistema de computador.
ms.assetid: 6241e703-4ce9-435f-bf36-4388e38a3ea5
ms.tgt_platform: multiple
title: Classe Win32_ComputerSystemProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProduct
- Win32_ComputerSystemProduct.Caption
- Win32_ComputerSystemProduct.Description
- Win32_ComputerSystemProduct.IdentifyingNumber
- Win32_ComputerSystemProduct.Name
- Win32_ComputerSystemProduct.SKUNumber
- Win32_ComputerSystemProduct.Vendor
- Win32_ComputerSystemProduct.Version
- Win32_ComputerSystemProduct.UUID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8cab3dc8679c606076eca2f5cf704867aa9833c9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089025"
---
# <a name="win32_computersystemproduct-class"></a>\_Classe Win32 ComputerSystemProduct

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ComputerSystemProduct do Win32** representa um produto. Isso inclui software e hardware usado neste sistema de computador.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B96-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystemProduct : CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
  string UUID;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ ComputerSystemProduct** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ ComputerSystemProduct** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrição textual do produto.

Esta propriedade é herdada [**do \_ produto CIM**](cim-product.md).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição textual do produto.

Esta propriedade é herdada [**do \_ produto CIM**](cim-product.md).

</dd> <dt>

**IdentifyingNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,4 ")
</dt> </dl>

Identificação do produto, como um número de série em software, um número de dado em um chip de hardware ou (para produtos comerciais) um número de projeto.

Esta propriedade é herdada [**do \_ produto CIM**](cim-product.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,2 ")
</dt> </dl>

Nome do produto usado normalmente.

Esta propriedade é herdada [**do \_ produto CIM**](cim-product.md).

</dd> <dt>

**SKUNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Informações de SKU (unidade de manutenção de estoque) do produto.

Esta propriedade é herdada [**do \_ produto CIM**](cim-product.md).

</dd> <dt>

**UUID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| UUID do tipo 1 do SMBIOS \| ")
</dt> </dl>

UUID (identificador universal exclusivo) para este produto. Um UUID é um identificador de 128 bits que é garantido para ser diferente de outros UUIDs gerados. Se um UUID não estiver disponível, um UUID de todos os zeros será usado.

Esse valor é proveniente do membro **UUID** da estrutura de **informações do sistema** nas informações do SMBIOS.

</dd> <dt>

**Fornecedor**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,1 ")
</dt> </dl>

Nome do fornecedor do produto ou a entidade que vende o produto (fabricante, revendedor, OEM e assim por diante).

Esta propriedade é herdada [**do \_ produto CIM**](cim-product.md).

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,3 ")
</dt> </dl>

Informações de versão do produto.

Esta propriedade é herdada [**do \_ produto CIM**](cim-product.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ ComputerSystemProduct** é derivada do [**\_ produto CIM**](cim-product.md).

## <a name="examples"></a>Exemplos

A amostra do [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell na galeria do TechNet usa o **Win32 \_ ComputerSystemProduct** para recuperar uma lista de hardwares que não funciona usando o WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Produto CIM**](cim-product.md)
</dt> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

