---
description: Representa os dados brutos de uma estrutura de dados de identificação de exibição estendida (E-EDID) avançada de uma associação padrão de eletrônicos de vídeo (VESA).
ms.assetid: a51b73bb-a5f7-4e01-9c88-780105e9952b
title: Classe WmiMonitorRawEEdidV1Block
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorRawEEdidV1Block
- WmiMonitorRawEEdidV1Block.Active
- WmiMonitorRawEEdidV1Block.InstanceName
- WmiMonitorRawEEdidV1Block.Id
- WmiMonitorRawEEdidV1Block.Type
- WmiMonitorRawEEdidV1Block.Content
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 79566dccceb36281c9b3a94b19fed2ed5679dc8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815452"
---
# <a name="wmimonitorraweedidv1block-class"></a>Classe WmiMonitorRawEEdidV1Block

A classe WMI **WmiMonitorRawEEdidV1Block** representa os dados brutos de uma estrutura de dados de identificação de exibição estendida (VESA) avançada de uma associação de vídeo (e-EDID). Essa estrutura de dados de 128 bytes contém informações que descrevem a configuração ideal para uma exibição.

## <a name="syntax"></a>Sintaxe

``` syntax
class WmiMonitorRawEEdidV1Block : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint8   Id;
  uint8   Type;
  uint8   Content[];
};
```

## <a name="members"></a>Membros

A classe **WmiMonitorRawEEdidV1Block** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **WmiMonitorRawEEdidV1Block** tem essas propriedades.

<dl> <dt>

**Ativo**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o monitor ativo.

</dd> <dt>

**Conteúdo**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

matriz de bytes de 128 que contém o conteúdo de bloco bruto.

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identidade do bloco de dados.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Nome da instância de monitor específica.

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de bloco de dados. A tabela a seguir lista os possíveis valores que podem ser retornados.



| Valor                                                                                 | Significado                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>    | Não Inicializado<br/>   |
| <dl> <dt>1 (0x1)</dt> </dl>    | Bloco base EDID<br/> |
| <dl> <dt>2 (0x2)</dt> </dl>    | Mapa de bloco EDID<br/>  |
| <dl> <dt>255 (0xFF)</dt> </dl> | Outro<br/>           |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | \\WMI raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> <dt>

[**WmiGetMonitorRawEEdidV1Block**](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md)
</dt> </dl>

 

 




