---
title: Classe Win32_RDSHCollection
description: Gerencia uma coleção de hosts de sessão de Área de Trabalho Remota.
ms.assetid: 7800bf2e-9497-4e41-aed9-b318748dd83f
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDSHCollection Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDSHCollection classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDSHCollection
- Win32_RDSHCollection.Alias
- Win32_RDSHCollection.Name
- Win32_RDSHCollection.Description
- Win32_RDSHCollection.Type
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8196747714337890d0b27ef6db8d488eedc32fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455267"
---
# <a name="win32_rdshcollection-class"></a>\_Classe Win32 RDSHCollection

Gerencia uma coleção de hosts de sessão de Área de Trabalho Remota.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHCollection
{
  string Alias;
  string Name;
  string Description;
  uint32 Type;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ RDSHCollection** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ RDSHCollection** tem esses métodos.



| Método                                                                      | Descrição                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getint32property**](getint32property-win32-rdshcollection.md)           | Recupera um valor da propriedade Integer de um objeto **\_ RDSHCollection do Win32** .<br/>                                                                                                                  |
| [**Getstringproperty**](getstringproperty-win32-rdshcollection.md)         | Recupera um valor de propriedade da cadeia de caracteres de um objeto **\_ RDSHCollection do Win32** .<br/>                                                                                                                    |
| [**KeyValueCompareAndSet**](win32-rdshcollection-keyvaluecompareandset.md) | Compara a chave especificada na coleção com um termo; Se eles corresponderem, a chave será definida como um novo valor. Se a chave não existir, o método irá inserir a chave na coleção.<br/> |
| [**KeyValueDelete**](win32-rdshcollection-keyvaluedelete.md)               | Exclui a chave especificada (e o valor associado) da coleção.<br/>                                                                                                                       |
| [**KeyValueGet**](win32-rdshcollection-keyvalueget.md)                     | Recupera o valor associado à chave especificada na coleção.<br/>                                                                                                                    |
| [**Setint32property**](setint32property-win32-rdshcollection.md)           | Atualiza um valor da propriedade Integer de um objeto **\_ RDSHCollection do Win32** .<br/>                                                                                                                    |
| [**Setstringproperty**](setstringproperty-win32-rdshcollection.md)         | Atualiza um valor de propriedade de cadeia de caracteres de um objeto **Win32 \_ RDSHCollection** .<br/>                                                                                                                      |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ RDSHCollection** tem essas propriedades.

<dl> <dt>

**Alias**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtém e define o alias da coleção.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtém e define a descrição da coleção.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obtém e define o nome da coleção.

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

**Windows server 2012 R2 e Windows server 2012:** Essa propriedade não está disponível antes do Windows Server 2016.

O tipo de coleção.

<dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**Regular** (0)


</dt> <dd></dd> <dt>



 (2)


</dt> <dd>

Reservado

</dd> <dt>



 (3)


</dt> <dd>

Reservado

</dd> <dt>

<span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>

<span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**ManualPersonal** (4)


</dt> <dd></dd> <dt>

<span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>

<span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**Pessoa física** (5)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\RDMs cimv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Provedor de serviços de gerenciamento de Área de Trabalho Remota](rdms-api-reference.md)
</dt> </dl>

 

