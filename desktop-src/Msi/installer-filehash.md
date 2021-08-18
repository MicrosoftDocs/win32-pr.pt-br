---
description: O método FileHash do Objeto do Instalador leva o caminho para um arquivo e retorna um hash de 128 bits desse arquivo. As informações de hash do arquivo são retornadas como um Objeto de Registro. Todo o hash de arquivo de 128 bits é retornado como quatro campos de propriedade IntegerData de 32 bits.
ms.assetid: 065ffde1-4d7c-4e71-9315-7926d4cd38ed
title: Método Installer.FileHash
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileHash
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a2da76ef3f0606002e26e8c320f83ca45e46bbbeb573d509c235c9fca8932247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630787"
---
# <a name="installerfilehash-method"></a>Método Installer.FileHash

O **método FileHash** do [**Objeto do Instalador**](installer-object.md) leva o caminho para um arquivo e retorna um hash de 128 bits desse arquivo. As informações de hash do arquivo são retornadas como um [**Objeto de Registro**](record-object.md). Todo o hash de arquivo de 128 bits é retornado como quatro campos de propriedade [**IntegerData**](record-integerdata.md) de 32 bits.

Os valores retornados no [**Objeto de**](record-object.md) Registro correspondem aos quatro campos da estrutura [**MSIFILEHASHINFO**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) retornados por [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha). A numeração de quatro campos é baseada em 1 na [tabela MsiFileHash](msifilehash-table.md).

-   O campo 1 corresponde à coluna HashPart1.
-   O campo 2 corresponde à coluna HashPart2.
-   O campo 3 corresponde à coluna HashPart3.
-   O campo 4 corresponde à coluna HashPart4.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.FileHash(
  FilePath,
  Options
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FilePath* 
</dt> <dd>

Caminho para o arquivo que deve ser com o hashed.

</dd> <dt>

*Opções* 
</dt> <dd>

Reservado para uso futuro.

O valor desse parâmetro deve ser 0 (zero).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedido, esse método retornará [**um Objeto de Registro**](record-object.md) que contém o hash do arquivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | O IInstaller IID é definido como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Versão do arquivo padrão](default-file-versioning.md)
</dt> <dt>

[Gerenciar tamanhos e versões de arquivos](manage-file-sizes-and-versions.md)
</dt> <dt>

[Tabela MsiFileHash](msifilehash-table.md)
</dt> <dt>

[**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> </dl>

 

 




