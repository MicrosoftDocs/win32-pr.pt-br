---
description: Renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto. Não há suporte para renomeação se o destino estiver em outra unidade ou se for necessário sobrepor um arquivo lógico existente.
ms.assetid: 728737a7-7cb8-4237-be03-16c4dac530b2
ms.tgt_platform: multiple
title: Renomear o método da CIM_Directory classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b9236b3384b8d945cea41c1a1fbe7b8db22f7ed70d692144e1691c6bfcf97270
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077476"
---
# <a name="rename-method-of-the-cim_directory-class"></a>Renomear o método da classe de diretório CIM \_

O **método Renomear** renomeia o arquivo lógico (ou diretório) especificado no caminho do objeto. Não há suporte para renomeação se o destino estiver em outra unidade ou se for necessário sobrepor um arquivo lógico existente.

Esse método é herdado de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FileName* \[ Em\]
</dt> <dd>

Nome totalmente qualificado do arquivo (ou diretório).

Exemplo: "c: \\ temp \\newname.txt"

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.

<dl> <dt>

**0**
</dt> <dd>

Êxito.

</dd> <dt>

**2**
</dt> <dd>

Acesso negado

</dd> <dt>

**8**
</dt> <dd>

Falha não especificada.

</dd> <dt>

**9**
</dt> <dd>

Objeto inválido.

</dd> <dt>

**10**
</dt> <dd>

O objeto já existe.

</dd> <dt>

**11**
</dt> <dd>

Sistema de arquivos não NTFS.

</dd> <dt>

**12**
</dt> <dd>

Plataforma não Windows.

</dd> <dt>

**13**
</dt> <dd>

A unidade não é a mesma.

</dd> <dt>

**14**
</dt> <dd>

O diretório não está vazio.

</dd> <dt>

**15**
</dt> <dd>

Violação de compartilhamento.

</dd> <dt>

**16**
</dt> <dd>

Arquivo inicial inválido.

</dd> <dt>

**17**
</dt> <dd>

Privilégio não mantido.

</dd> <dt>

**21**
</dt> <dd>

Parâmetro inválido.

</dd> </dl>

## <a name="remarks"></a>Comentários

Atualmente, esse método não é implementado pelo WMI. Para usar esse método, você deve implementá-lo em seu próprio provedor.

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

[Diretório \_ CIM](rename-method-in-class-cim-directory.md)
</dt> <dt>

[**Diretório \_ CIM**](cim-directory.md)
</dt> </dl>

 

