---
description: A classe Montagem CIM \_ representa uma associação entre um sistema de arquivos e um diretório ao qual ele está anexado.
ms.assetid: abf1833b-9b39-45c0-8400-2be2bf3a1c3c
ms.tgt_platform: multiple
title: CIM_Mount classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Mount
- CIM_Mount.Dependent
- CIM_Mount.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1298c695237ac40097b0c081d313769ee4e4e1190571b1bdd58137e25d53c10a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821016"
---
# <a name="cim_mount-class"></a>Classe de \_ montagem CIM

A **classe \_ Montagem CIM** representa uma associação entre um sistema de arquivos e um diretório ao qual ele está anexado.

A semântica dessa relação exige que o diretório montado seja contido por um sistema de arquivos (por meio da associação de armazenamento de arquivos) diferente do sistema de arquivos referenciado como dependente. O sistema de arquivos que contém o diretório pode ser local ou remoto. Por exemplo, um sistema de arquivos local em um sistema de computadores Solaris pode montar um diretório do sistema de arquivos acessado por meio da unidade CDROM do computador (ou seja, outro sistema de arquivos local). Por outro lado, em um caso "remoto", o diretório é exportado primeiro por seu sistema de arquivos, que é hospedado em outro sistema de computador que atua, por exemplo, como um servidor de arquivos. Para distinguir as duas montagens, uma associação [**de \_ Exportação cim**](cim-export.md) sempre deve ser definida para os diretórios acessados/montados remotamente.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{75BCF4F6-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Mount : CIM_Dependency
{
  CIM_NFS       REF Dependent;
  CIM_Directory REF Antecedent;
};
```

## <a name="members"></a>Membros

A **classe \_ Montagem CIM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ Montagem CIM** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Diretório CIM \_**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Um [**Diretório CIM \_**](cim-directory.md) que descreve o diretório montado.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ CIM NFS**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente")
</dt> </dl>

Um [**\_ NFS cim que**](cim-nfs.md) descreve o FileSystem no qual o diretório está montado.

</dd> </dl>

## <a name="remarks"></a>Comentários

**CIM \_ A** montagem é derivada da [**\_ Dependência CIM.**](cim-dependency.md)

O WMI não implementa essa classe.

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Dependência cim \_**](cim-dependency.md)
</dt> </dl>

 

